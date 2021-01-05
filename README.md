# battlesnake-nessegrev

This is a release of my current snakes.

The goal of the release is to let developers to use them to test their snakes via the [BattleSnake-CLI](https://github.com/BattlesnakeOfficial/rules/tree/master/cli)
You won't be able to use those snakes to run on [BattleSnake](https://play.battlesnake.com) because my snakes are "Author" protected. 

##Snake description

(In order of the stupiest snake to the little less stupid snake)

* Basic (aka Nessegrev): A clueless snake that try to go to the nearest food, only able to avoid wall and snakes bodies
* FloodFill (aka Nessegrev-flood): My first snake that enter a tournament (Stay Home and Code / Rookie division) This snake use FloodFill algorithm to find the best move. it try to target food and shorter snakes, and it try to avoid bigger snakes.
* Alpha : This snake participated in the Communitech tournament in the Rookie division. Still have some search bugs. It used some minMax algorithm
* Beta : This snake was in the summer league / veteran division. Still active on the global arena. Based on the Alpha snake, but fewer bugs and bit quicker.  Decent snake using minMax algorithm only
* Gamma: This snake was in the fall league and in the winter classic. Based on Beta snake, but with some "Area control" features. About as good as Beta.


## Properties files

Each snake has a properties file. You can edit it with any text editor. If you change the file, you need to restart the snake.
Most of the basic properties are self-explain, but the "minusbuffer" a millisecond property to compensate the latency. Example if the timeout is 500 ms,  and the minusbuffer is 150ms than the snake will use 350ms.
Please take note that sometimes (maybe cause by java garbage collection) my snakes may timeout.

## How to
test