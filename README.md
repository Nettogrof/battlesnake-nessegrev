# Battlesnake-nessegrev

This is a release of my current snakes.

The goal of the release is to let developers to use them to test their snakes via the [BattleSnake-CLI](https://github.com/BattlesnakeOfficial/rules/tree/master/cli) or with [Mojave](https://github.com/smallsco/mojave).
You won't be able to use those snakes to run on [BattleSnake](https://play.battlesnake.com) because my snakes are "Author" protected. 

## Snake description

(In order of the stupiest snake to the little less stupid snake)

* Basic (aka Nessegrev): A clueless snake that try to go to the nearest food, only able to avoid wall and snakes bodies
* FloodFill (aka Nessegrev-flood): My first snake that enter a tournament ( [Stay Home and Code / Rookie division](https://play.battlesnake.com/competitions/stay-home-and-code/) ) This snake use FloodFill algorithm to find the best move. it try to target food and shorter snakes, and it try to avoid bigger snakes.
* Alpha : This snake participated in the [Communitech tournament](https://play.battlesnake.com/competitions/communitech/) in the Rookie division. Still have some search bugs. It used some minMax algorithm
* Beta : This snake was in the [summer league / veteran division](https://play.battlesnake.com/competitions/summer-league/). Still active on the global arena. Based on the Alpha snake, but fewer bugs and bit quicker.  Decent snake using minMax/payoff matrix algorithm only. This snake can play standard, squad, Royale.
* Gamma : This snake was in the fall league and in the [winter classic](https://play.battlesnake.com/competitions/winter-classic-2020/) in elite division. Based on Beta snake, but with some "Area control" features. With the new release Gamma is now more Duel oriented.  Doesn't take hazard into account.


## Properties files

Each snake has a properties file. You can edit it with any text editor. If you change the file, you need to restart the snake.
Most of the basic properties are self-explain, but the "minusbuffer" a millisecond property to compensate the latency. Example if the timeout is 500 ms,  and the minusbuffer is 150ms than the snake will use 350ms.
Please take note that sometimes (maybe cause by java garbage collection) my snakes may timeout.

## How-to

To run a snake, you need java installed  (any recent version).
In command line, type "java -jar snake.jar <SnakeName>"   example :  "java -jar snake.jar Beta" 

For Alpha, Beta and Gamma, you may add memory config  example : "java  -Xmx1024m -Xms1024m -jar snake.jar Beta"

The snake will listen on the port number from the .properties file.


# Release note

## 2021-03-09   New release
* Gamma and Beta can now be multitread.
* Fixed the issue that Gamma / Beta wasn't able to play on a non-squared board.
* Improve Gamma area control algorithm
* Few performances adjustement.
