---
title: "Commentary on SphinxTrain1.07's bw (Part II : next_state_utt.c's First Half)"
date: 2013-01-24
categories: ["bw", "state sequence"]
---

# Commentary on SphinxTrain1.07's bw (Part II : next_state_utt.c's First Half)

I will go on with the analysis of bw. In my [last post](http://grandjanitor.blogspot.com/2013/01/commentary-on-sphinxtrain107s-bw-part-i.html), we understand the high-level structure of the bw program. So we now turns to the details of how the state lattice was built. Or how next_state_utt.c works.

As always, here is the standard disclaimer: this is another long and super technical post I only expect a small group of programmer with exoteric interest of Baum-Welch algorithm can read. It's not for faint of heart but if you understand the whole thing, you would have some basic but genuine understanding of Baum-Welch algorithm in real life.

The name of the module, next_state_utt.c, is quite unassuming but it is an important key of understanding the Baum-Welch algorithm. The way how the state lattice is structured affects how parameter estimation works. The same statement says for not only Baum-Welch estimation but also other estimation algorithm in speech.

But what so difficult about the coding the lattice? Here are two points I think it is worthwhile to point out:

1. I guess an average programmer can probably work out a correct concatenation of all phone HMMs if all phones are context-independent in 3 days to 1 week. But in many advanced systems, most of them are using **context-dependent phones**. So you go to make sure at the right time, the right triphone state was used.
2. In Sphinx, it got a bit more complicated because there is a distinction between positions of triphones. This is quite specific to Sphinx and you won't find it in systems such as HTK. So it further complicates coding. You will see in the following discussion, Sphinx has back off cases of position-dependent triphone estimation from time-to-time. In my view, it might not be too different from the position-independent triphone system. (It's certainly fun to read. :) )

My goal here is to analyze the next_state_utt.c, how it works and to state some part one can improve.

#### High-Level Layout of next_utt_state.c:

```
 next_utt_state.c  
 -> mk_wordlist (mk_wordlist.c)  
 -> mk_phone_list (mk_phonelist.c)  
 -> cvt2triphone (cvt2triphone.c)  
 -> state_seq_make (state_seq_make.c)  
```

Nothing fancy here. We first make a wordlist (*mk_wordlist)* , then make a phone list *(mk_phone_list)*, then convert the phone list to triphone (*cvt2triphones*), then create the state sequence (*state_seq_make)*.

Now before we go on, just at this level, you may already discover one issue of Sphinx's bw. It is using a list to represent phone models. So, let's assume if you want to model a certain word with multiple pronunciations, you probably can't do it without changing the code.

Another important thing to note: just like many non-WFST systems, it is not that easy to make a simple phoneme system with Sphinx. (HTK is an exception but you can always turn on a flag to expand context. Just look up the manual.) Say if you want to express your phoneme system to be one phoneme word, then you would want your dictionary look like:

AA AA  
AE AE  
B B  
.  
.  
.  
.  
.

But then, if a word is a phone, should you actually want to build a network of cross-word triphones? You probably want to if you want to shoot for performance - all of the most accurate phoneme-based system has some sort of context-dependency there. (The Brno's recognizer probably has some, but I don't really grok why it is so good.)

But if you want to do your own interesting experiments, this fixed behavior may not suit your appetite. Maybe you just want to use a context-independent phone system for some toy experiments. But then, you are probably always building a triphone system. So, it might or might not be what you like.

So if you really want to trigger the CI-model behavior, what can you do? Take a look of my next post, in cvt2triphone.c, if the model definition file only specify CI states, then no triphone conversion will occur. In a way, that is to say the system assume if you just train the CI model, you will get the CI model but there is no explicit way to turn it off.

***mk_wordlist***   
**  
***mk_wordlist* is rather trivial:

```
 char **mk_wordlist(char *str,  
             uint32 *n_word)  
 {  
   uint32 n_w;  
   uint32 i;  
   char **wl;  
   n_w = n_words(str);  
   wl = ckd_calloc(n_w, sizeof(char *));  
   wl[0] = strtok(str, " t");  
   for (i = 1; i < n_w; i++) {  
      wl[i] = strtok(NULL, " t");  
   }  
   assert(strtok(NULL, " t") == NULL);  
   *n_word = n_w;  
   return wl;  
 }  

```

With one line of transcripts, *mk_wordlist* transform it to an array of C-string. Memory of the string are allocated.

***mk_phone_list***  
***  
****mk_phone_list* is still trivial but there is a bit more detail*.*   
*  
**  
*   

```
1:  acmod_id_t *mk_phone_list(char **btw_mark,  
2:                  uint32 *n_phone,  
3:                  char **word,  
4:                  uint32 n_word,  
5:                  lexicon_t *lex)  
6:  {  
7:    uint32 n_p;  
8:    lex_entry_t *e;  
9:    char *btw;  
10:    unsigned int i, j, k;  
11:    acmod_id_t *p;  
12:    /*  
13:     * Determine the # of phones in the sequence.  
14:     */  
15:    for (i = 0, n_p = 0; i < n_word; i++) {  
16:       e = lexicon_lookup(lex, word[i]);  
17:       if (e == NULL) {  
18:         E_WARN("Unable to lookup word '%s' in the lexiconn", word[i]);  
19:         return NULL;  
20:       }  
21:       n_p += e->phone_cnt;  
22:    }  
23:    /*  
24:     * Allocate the phone sequence  
25:     */  
26:    p = ckd_calloc(n_p, sizeof(acmod_id_t));  
27:    /*  
28:     * Allocate the between word markers  
29:     */  
30:    btw = ckd_calloc(n_p, sizeof(char));  
31:    for (i = 0, k = 0; i < n_word; i++) {     /* for each word */  
32:       e = lexicon_lookup(lex, word[i]);  
33:       if (e->phone_cnt == 0) /* Ignore words with no pronunciation */  
34:        continue;  
35:       for (j = 0; j < e->phone_cnt-1; j++, k++) {     /* for all but the last phone in the word */  
36:         p[k] = e->ci_acmod_id[j];  
37:       }  
38:       p[k] = e->ci_acmod_id[j];     /* move over the last phone */  
39:       btw[k] = TRUE;               /* mark word boundary following  
40:                             kth phone */  
41:       ++k;  
42:    }  
43:    *btw_mark = btw;  
44:    *n_phone = n_p;  
45:    assert(k == n_p);  
46:    return p;  
47:  }  

```

In line 15-22:, we first look up the pronunciations of the words. (Remember, right now we can only look up one.) It then allocate the an array of phones with ID (in the type of *acmod_id_t*).

Now here is special part of the code, other the array of phones, it also allocate an array call "between word markers". So what's the mechanism? Let me give an example.

Suppose you have a transcript with word sequence "MY NAME IS CLINTON"

mk_word_list would create

```
     word[0] -> MY  
     word[1] -> NAME  
     word[2] -> IS  
     word[3] -> CLINTON  

```

mk_print_list (with my best guess of pronunciations) would create  

```
     ph[0] -> M      btw[0] -> 0
     ph[1] -> AY      btw[1] -> 1
     ph[2] -> N      btw[2] -> 0
     ph[3] -> EY      btw[3] -> 0
     ph[4] -> M      btw[4] -> 1
     ph[5] -> IY      btw[5] -> 0
     ph[6] -> S      btw[6] -> 1
     ph[7] -> K      btw[7] -> 0
     ph[8] -> L      btw[8] -> 0
     ph[9] -> IY      btw[9] -> 0
     ph[10] -> N      btw[10] -> 0
     ph[11] -> T      btw[11] -> 0
     ph[12] -> AX     btw[12] -> 0
     pH[13] -> N      btw[13] -> 1

```

So essentially it would indicate there is a word end at a certain phone. 

I believe such as representation are for convenience purpose: it facilitate determination of whether a word is at the beginning, the middle or the end.

An alternative here is to do an optional silence. This, according to HTK handbook, usually reduce the WER slightly. It seems to be reasonable to figure out where the location of a phone is using silences as a marker.

#### ***A digression: acmod_id_t***

```
1:  typedef unsigned char ci_acmod_id_t;  
2:  #define NO_CI_ACMOD     (0xff)  
3:  #define MAX_CI_ACMOD     (0xfe)  
4:  typedef uint32 acmod_id_t;  
5:  #define NO_ACMOD     (0xffffffff)     /* The ID representing no acoustic  
6:                            * model. */  
7:  #define MAX_ACMOD     (0xfffffffe)     /* The max ID possible */  

```

Now, we used *acmod_id_t* in *mk_phone_list*, but what is it really? So let's take a detour of *acmod_id_ds.t* (*"ds"* stands for data structure.)

*acmod_id_t* is essentially a *uint32*, which is just a the size of unsigned integer or 2^32 -1. Why -1? Notice that *MAX_CI_ACMOD* was defined as *0xfe*?

The more interesting part here: we saw *ci_acmod_id_t* is only a character type. This is obviously another problem here, in some languages, one may be interested to express it with more than 255 phones. (Why 255?)

We'll meet acmod_set a little bit more. But let us move on first - sometimes code tracing will be more motivated when you see the code before the data structure. Many suggest otherwise: Indeed, once you know the data, code will make more sense. But in practice, you will most likely read the code first and needs to connect things together. Thus IMO: both approach has their merit in code tracing.

#### **So far ..... and next post**

To avoid clutter a single post, I will stop and put the rest of next_utt_states.c (*cvt2phones and state_seq_make)* on another post. But I want to summarize several things I have observed so far:

1. Current bw doesn't create a word network so it has issues to handle multiple pronunciations.
2. Current bw automatically expand triphone contexts. There is no explicit way to turn it off.
3. bw is not doing optional silence in the network.
4. bw doesn't work for more than 255 CI phones.

Btw, SphinxTrain1.08 has several changed which replace mk_word_list with data structure from sphinxbase. Those are encouraging changes. If I have time, I will cover them. 

Arthur

---

## Comments

**三十三博** (2013-01-26):

Thanks!

**Elias Majic** (2013-01-26):

Hi Arthur,
I added you on twitter.

**三十三博** (2013-01-26):

Sure Elias,

From time to time, I will add more content on this site.

If you want to catch up with updates, subscribe "Grand Janitor" with RSS/Twitter or include me in Plus.

Arthur

**Elias Majic** (2013-01-26):

These are great blog posts. I would vote for more training blog posts.

**Elias Majic** (2013-01-26):

These are great blog posts. I would vote for more training blog posts.

**三十三博** (2013-02-25):

Mr. Anonymous,

You might want to follow the basic training tutorial from cmusphinx.org.

http://cmusphinx.sourceforge.net/wiki/tutorialam

I do plan to write more tutorial material on this blog. Just that I am a little bit busy. Hopefully later......

**602e03f4-2327-11e2-8544-000bcdcb8a73** (2013-02-25):

Hi,

If I just want to create the mdef file, from transcription and dictionary files, how should I go about it?

