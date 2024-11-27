# MayhemAtomic

Linux Xboard Atomic Chess Engine.

![logo](https://github.com/user-attachments/assets/b31bb923-06ef-4bb1-89ce-1f54982766f3)


## Supported Commands

```
MayhemAtomic. Linux Xboard Atomic Chess engine. Written in C++20 language

Supported commands:

help
  This help

ping [N]
  Responded by 'pong N'

level [movestogo] [time] [inc]
  Setup time control

random
  Add random element to eval

time [N]
  Setup time left for the engine

force
  Setup force mode. Act only after 'go' command

new
  Setup new game

list
  Show list of moves

play [ms = 5000]
  Watch a game

analyze
  Analyze position

undo
  Go back in history

.
  Respond ASAP

?
  Move ASAP

option
  Setup option in form of 'option hash=256'

variant
  Setup variant

setboard
  Setup board using FEN notation

logo
  Print ASCII art logo

p [fen = startpos]
  Print ASCII art board

perft [depth = 6] [fen = startpos]
  Calculate perft split numbers

bench [depth = 14]
  Show signature of the program

bits N
  Show bits of N

speed [ms = 5000]
  Show speed of the program

exit
  Exits the analyze mode

quit
  Exits the engine ASAP
```

## Tests

```
Finished game 1000 (MayhemAtomic 0.1 vs MayhemAtomic 0.1): 1-0 {Black's king exploded}
Score of MayhemAtomic 0.1 vs MayhemAtomic 0.1: 457 - 454 - 89  [0.501] 1000
...      MayhemAtomic 0.1 playing White: 235 - 216 - 49  [0.519] 500
...      MayhemAtomic 0.1 playing Black: 222 - 238 - 40  [0.484] 500
...      White vs Black: 473 - 438 - 89  [0.517] 1000
Elo difference: 1.0 +/- 20.5, LOS: 54.0 %, DrawRatio: 8.9 %
SPRT: llr 0 (0.0%), lbound -inf, ubound inf

Player: MayhemAtomic 0.1
   "Draw by 3-fold repetition": 76
   "Draw by fifty moves rule": 6
   "Draw by stalemate": 7
   "Loss: Black mates": 81
   "Loss: Black's king exploded": 141
   "Loss: White mates": 97
   "Loss: White's king exploded": 135
   "Win: Black mates": 64
   "Win: Black's king exploded": 124
   "Win: White mates": 111
   "Win: White's king exploded": 158
Player: MayhemAtomic 0.1
   "Draw by 3-fold repetition": 76
   "Draw by fifty moves rule": 6
   "Draw by stalemate": 7
   "Loss: Black mates": 64
   "Loss: Black's king exploded": 124
   "Loss: White mates": 111
   "Loss: White's king exploded": 158
   "Win: Black mates": 81
   "Win: Black's king exploded": 141
   "Win: White mates": 97
   "Win: White's king exploded": 135
Finished match
```

## Sample game

```
[White "MayhemAtomic 0.1"]
[Black "MayhemAtomic 0.1"]
[Result "1-0"]
[TimeControl "60+1"]
[Variant "atomic"]
[FEN "rnbbknqr/pppppppp/8/8/8/8/PPPPPPPP/RNBBKNQR w KQkq - 0 1"]
1. Ng3 {+0,60/15} d6 {-0,54/16 3} 2. Nc3 {+0,69/16 3} c6 {-0,58/16 3} 3.
Nf5 {+0,67/15 3} Bxf5 {-0,45/17 3} 4. d3 {+0,52/16 3} Bb6 {-0,50/16 3} 5.
e3 {+0,46/18 3} Ng6 {-0,34/17 3} 6. Bh5 {+0,54/16 2,9} a5 {-0,65/16 2,9} 7.
Na4 {+0,68/17 2,8} Nd7 {-0,51/16 2,8} 8. Nc5 {+0,54/15 2,7} Bxc5
{-0,67/17 2,7} 9. e4 {+0,45/15 2,7} h6 {-0,61/15 2,7} 10. f4 {+0,69/16 2,6}
c5 {-0,59/16 2,6} 11. Qf2 {+0,67/16 2,5} O-O-O {-0,55/15 2,5} 12. Bg4
{+0,93/16 2,5} e6 {-0,89/18 2,5} 13. f5 {+0,86/17 2,4} Nh4 {-0,73/18 2,4}
14. fxe6 {+0,71/17 2,4} f5 {-0,65/18 2,4} 15. Qd2 {+0,71/16 2,3} Qf7
{-0,67/16 2,3} 16. b3 {+0,75/15 2,3} Qc7 {-0,83/16 2,3} 17. c4
{+0,85/15 2,2} Nxg2 {-0,80/15 2,2} 18. Bb2 {+0,87/16 2,2} d5 {-1,10/16 2,2}
19. Bxg7 {+0,90/16 2,1} fxg4 {-1,02/16 2,1} 20. O-O-O {+1,04/17 2,1} Rg8
{-1,15/16 2,1} 21. Rf1 {+1,17/17 2,0} Rg2 {-0,87/15 2,0} 22. Kb1
{+1,17/15 2,0} Rf2 {-1,20/16 2,0} 23. Rxf2 {+1,11/18 1,9} Qf7
{-1,16/18 1,9} 24. e5 {+1,58/17 1,9} Qf1 {-1,36/15 1,9} 25. Qd1
{+1,50/19 1,9} Qg2 {-1,59/18 1,9} 26. Qe2 {+1,56/19 1,8} b5 {-1,42/17 1,8}
27. Qxg2 {+1,58/18 1,8} Kd8 {-2,19/21 1,8} 28. e6 {+2,79/19 1,8} Ke7
{-2,79/20 1,8} 29. a4 {+3,17/18 1,7} h5 {-3,40/17 1,7} 30. h4
{+9,97/17 1,7} Kf8 {-10,12/16 1,7} 31. e7 {+104,85/20 0,1} Ke8
{-104,85/19 0,2} 32. cxb5 {+104,85/14} d4 {-104,85/11} 33. Kc2 {+104,85/10}
c4 {-104,85/9} 34. bxc4 {+104,85/8} Kd7 {-104,85/7} 35. e8=Q {+104,85/6}
Kc7 {-104,85/5} 36. Qc6 {+104,85/4} Kd8 {-104,85/3} 37. Qd7 {+104,85/2}
{ White Wins } 1-0
```
