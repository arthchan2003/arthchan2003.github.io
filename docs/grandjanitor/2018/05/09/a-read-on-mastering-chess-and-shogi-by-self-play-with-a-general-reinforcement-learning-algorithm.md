---
title: "A Read on \" Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm\""
date: 2018-05-09
---

# A Read on " Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm"

(First published at AIDL Weekly and AIDL-LD.)

[Kade Gibson](https://www.facebook.com/i92.i68.i.i?fref=gs&dti=849857175178950&hc_location=group) already post this paper and give a good summary. I want to analyze it with a more detail so I started a separate thread.

\* As you know the story, AlphaZero is not only just playing Go, and is now playing Chess and Shogi. By itself this is a significant event, because most stoa board game engine are specific to games. General game playing engines are seen as novelties but not a norm.

\* Another note, most Chess and Shogi engines are based on alpha-beta search. But then AlphaZero is now using Monte-Carlo Tree Search which simulate board positions. Positions are order by scores from a board NN. State is entered in the order of visit counts and value of the board according to NN. So you can see this is not just AlphaZero is beating up more games, it will be more a paradigm shift of both computer Chess and Shogi community. 

\* As you know, AlphaZero beats the strongest program in 2016, Stockfish. But one analysis which caught my eyes: In chess, DeepMind researchers also fix the first few moves of AlphaZero so that it follows the top 12 most-play openings for black and white. If you are into chess, Queen's Gambit, several Sicilian Defences, The French, KID. They show that AlphaZero can beat Stockfish in multiple type of situations, and openings doesn't matter too much.

\* But then, would AlphaZero beat all computer players such as Shredder or Komodo? No one knows the answers yet.

\* One more thing: AlphaZero doesn't assume zero knowledge neither. As Denny Britz points out in his tweet, AlphaZero was provided with perfect knowledge in terms of rules. So intriguing rules such as castling, threefold repetition or 50-move drawing rules are all provided to the machine. Perhaps Britz points out, may be we want to focus on how to let the machine to figure out the rules themselves in the future.

That's what I have. Hope you enjoy it.
