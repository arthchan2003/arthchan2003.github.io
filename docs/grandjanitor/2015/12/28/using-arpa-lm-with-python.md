---
title: "Using ARPA LM with Python"
date: 2015-12-28
---

# Using ARPA LM with Python

During Christmas, I tried to do some small fun hack with language modeling. That obviously requires *reading* and *evaluating* an LM. There are many ways to do so. But here is new method which I really like: [use the python interface of KenLM.](http://victor.chahuneau.fr/notes/2012/07/03/kenlm.html)

So here is a note for myself (largely adapted from Victor Chahuneau): 

## Install boost-1.6.0

To install KenLM, you need to first install boost. If you want to install boost, then you need to install libbz2. 
1. First, install libbz2: 

    ```
    sudo apt-get install libbz2-dev
    ```
2. Then install 1.6.0: download [here](http://sourceforge.net/projects/boost/files/boost/1.60.0/), then type 

    ```
    ./bootstrap.sh
    ```

    , and finally 

    ```
    ./bj2 -j 4
    ```
3. Install boost: 

    ```
    ./bj2 install
    ```

## Install KenLM

Now we install kenlm, I am using the copy of Victor's here. 

```
git clone https://github.com/vchahun/kenlm.git
pushd kenlm
./bjam
python setup.py install
popd

```

## Training an LM

Download some books from Gutenberg, I am using *[Chambers's Journal of Popular Literature, Science, and Art, No. 723](http://www.gutenberg.org/files/50780/50780-0.txt).* And I got this file,

`50780-0.txt ` So all you need to do to train a model is, 

```
cat 50780-0.txt| /home/archan/src/github/kenlm/bin/lmplz -o 3 > yourLM.arpa

```

Then you can binarize the LM, which is the part I like about KenLM, it feels snappy and fast than other toolkits I used. 

```
/home/archan/src/github/kenlm/bin/build_binary yourLM.arpa yourLM.klm
```

## Evaluate a Sentence with an LM

Write a python script like this: 

```
import kenlm
model = kenlm.LanguageModel('yourLM.klm')
score = model.score('i like science fiction')
print score
```

Arthur
