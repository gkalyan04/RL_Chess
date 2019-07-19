# About
Here you can find some code<sup>[[1]](#myfootnote1)</sup> about implementation of chess engine via reinforcement learning of [AlphaZero methods](https://arxiv.org/pdf/1712.01815.pdf).

## Supervised Learning
Supervised learning could be done over PGN games files of professional chess players (with high elo rating that means). This data was taken from the chess database called [FICS](http://ficsgames.org/download.html).

Here some nice results (over 3000 games of SL, elo >= 2000). I'm (white) playing against the program (black):

![alt text](https://github.com/andynik/deep-move/blob/master/images/ApronusDiagram1529753143.gif 'I am vs program')

To start SL put PGN files in `data/play_data` dir and run the command:

```
python src/chess_zero/run.py sl
```

## Reinforcement Learning
For reinforcement learning use: `self`, `opt` and `eval` commands:

Command | Description
--- | ---
`self` | is Self-Play to generate training data by self-play using BestModel
`opt` | is Trainer to train model and generate next-generation models
`eval` | is Evaluator to evaluate whether the next-generation model is better than BestModel. If better, replace BestModel

All in all it's just about generating PGN data which contains self-played games by the chess engine.

