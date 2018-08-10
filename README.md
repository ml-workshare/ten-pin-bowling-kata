# ten-pin-bowling-kata

How Ten Pin Bowling Scoring Works
---------------------------------
Ten pin bowling is a game that consists of ten "frames". In each frame, each player has two chances to knock down ten pins. The score for the frame is the total number of pins knocked down, plus a bonus for "strikes" or "spares.

A "strike" is when the player has knocked down all ten pins on the first try for that frame. When this happens, the bonus for the frame is the value of the next two balls rolled.

Example: In frame 1, the player knocks down all 10 pins on the first go. In frame 2, the player knocks down 7 on the first attempt, then 1 on the second attempt. The total score for frame 1 is 18.

A "spare" is when the player has knocked down all ten pins in two tries. When this happens, the bonus is the number of pins knocked down by the next roll.

Example: In frame 1, the player knocks down 5 pins on the first go, and 5 pins on the second go. In frame 2, the player knocks down 7 on the first attempt, then 1 on the second attempt. The total score for Frame 1 is 17.

For the tenth frame, a player who has knocked down all ten pins is allowed a third roll. The score for the tenth frame is the total number of pins knocked down in that frame.

Example: In frame 10, the player knocks down 5 pins on the first go, 5 pins on the second go. The player has scored a "Spare" so is allowed roll a total of three times in the frame (instead of the normal 2). The player knocks down 10 pins on the last go. The total score for the frame is 20.

Example: In frame 10, the player knocks down 10 pins on the first go. The player has scored a "Strike" so is allowed to roll three times in the frame (instead of the normal 2). The player knocks down 10 pins on the second attempt, then 10 on the final go. The toal score is 30.

The total score for the game is the total score for each frame.

Challenge objectives
``` c#
public interface IBowlingGame 
{
     // called each time a player rolls a ball
     void Roll(int pins);

     // called at the end of the game to retrieve total score
     int FinalScore();
}
```

The task is to implement IBowlingGame.

Example game:

Frame # | Rolls | Cumulative Score
--------|-------|------
1       | 9, 1  | 10
2       | 0, 10 | 30
3       | 10    | 56
4       | 10    | 74
5       | 6, 2  | 82
6       | 7, 3  | 100
7       | 8, 2  | 120
8       | 10    | 139
9       | 9, 0  | 148
10      | 10, 10, 8 | 176 
