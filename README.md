# Group Project: World's Hardest Game

[![Run on Repl.it](https://repl.it/badge/github/upperlinecode/worlds-hardest-game-javascript)](https://repl.it/github/upperlinecode/worlds-hardest-game-javascript)

## The Goal

Today, we're going to build a game resembling the apparent world's hardest, which you should try the first level of [here](https://www.coolmathgames.com/0-worlds-hardest-game). You're game doesn't have to be exactly the same, but try to build something on the idea of a player moving around trying to dodge things.

## A Possible Beginning

### Step One: Moving the player

1. Create a small blue circle on screen which will represent the player.

2. Create an object called `player` with properties `x` and a `y` to store the player's position. Initialize these to reasonable on-screen values. Then change the call to `ellipse` to draw the player dynamically based on this new object.

3. Create a definition for `keyPressed` and add four conditionals which will move the player, one for each direction. The conditional to move the player left should check if `keyCode === LEFT_ARROW` and if so, should decrease `player.x` by a small amount.

### Step Two: A basic enemy

1. Create a second object called `enemy1` with `x` and `y` components, and initialize them to reasonable values as well. Then draw a small red circle at `(enemy1.x, enemy1.y)`.

2. Let's have this enemy move left to right. To keep track of which way it's going, add a third property to `enemy1` called `movingLeft`, and set this initially to `true`.

3. In the draw loop. change `enemy1.x` according to `enemy1.movingLeft`. That is, if `movingLeft` is `true`, decrease `x` by a small amount and otherwise increase it.

4. Then, set bounds for `movingLeft` at which point it will reverse. The left bound could, for example, check if `enemy1.x < 100` and if so, could set `enemy1.movingLeft` to `false`.

### Step Three: Winning and losing

1. When the player comes in contact with the enemy, you'd probably like for something to happen. The simplest would be to reset the player's position to a starting zone. Perhaps you want to draw a green rectangle to show where that starting zone is.

2. This would also be a good time to add a winning zone, which you can also illustrate with green. When the player enters this zone (which you'll likely need four conditionals to verify), what exactly should happen? In the future, you might add a second level for the player to advance to. Now you could just gain a point or change the enemy's position or what have you.

### Step Four: More enemies

1. To make the game interesting, you'll probably want more than one enemy. You can create more variables (`enemy2`, `enemy3`, etc.) to hold as many as you'd like.

2. You' also might want enemies that move vertically instead of horizontally. The code should look similar, so see if you can figure it out.

### Step Five: Walls

1. In order to force the player to dodge enemies instead of just walking around them, you'll likely want to add walls. You can start by drawing your walls with simple black lines.

2. Now think about how you could stop the player from walking through these walls. A set of conditionals in `keyPressed` could be the best way to go about this. For example, you could use two conditionals for each wall to stop the player from moving through from each side.
