# PING-PONG game

## Youtube video of the game

https://www.youtube.com/watch?v=5WfX-oKqDFI

#### About game

Game is based on one player and one ball. Goal is that paddle keeps ball bouncing around the screen, if ball doesn't hit paddle it's game over. New game start when player presses button for restart. There are also speed up and slow down buttons for paddle movement, in case player is far from the ball so he can catch up.

##### Controls

1. board move right "->"
2. board move left "<-"
3. restart "A"
4. speed up board "Z"
5. speed down board "B"

###### Function of moving ball

1. If board doesn't move, ball will continue to move in normal trajectrory.
2. if board moves in opposite direction compared to ball nothing really changes here.

Plot twist is in the next segment
3. If board moves in the same direction as ball (left or right) ball will bounce in the way it came from.

###### Bonus. Main logic explained
Complex physics such as bouncing in diferent angles depending of paddle speed and adding blocks would requier more time.
First there must me if loop to encompass whole paddle width

if((bs.gameball.x >= gs.paddle.x && bs.gameball.x <= gs.paddle.x + PADDLE_W)){
	
in that loop must be six other loops for every possible outcome. There is example of one of them in witch ball is hitting paddle from the left while paddle is standing still		
		if(bs.gameball.y == SCREEN_H-GAME_BALL-PADDLE_H && bs.gameball.x < SCREEN_W-GAME_BALL && x == 2 && y == 2 && dir == 0) {
    	x = 2;
			y = -2;
      }
      }
1. first we check y (height) coordinates
2. then x (width) 
3. then trajetrory of the ball
4. and finnaly direction in which paddle is moving
		
