# Battlesnake-nessegrev

This is a release of my current snakes.

The goal of the release is to let developers to use them to test their snakes via the [Battlesnake CLI](https://github.com/BattlesnakeOfficial/rules/tree/master/cli) or with [Mojave](https://github.com/smallsco/mojave).
You won't be able to use those snakes to run on [Battlesnake](https://play.battlesnake.com) because my snakes are "Author" protected.

## Snake description

(In order of the stupidest snake to the slightly less stupid snakes)

* Basic (aka Nessegrev): A clueless snake that tries to go to the nearest food, only able to avoid wall and snakes' bodies
* FloodFill (aka Nessegrev-flood): My first snake that I entered in a tournament ([Stay Home and Code / Rookie division](https://play.battlesnake.com/competitions/stay-home-and-code/)) This snake use flood fill algorithm to find the best move. It tries to target food and shorter snakes, and avoids bigger snakes.
* Alpha : This snake participated in the [Communitech tournament](https://play.battlesnake.com/competitions/communitech/) in the Rookie division. Still has some search bugs. It uses the minimax algorithm
* Beta : This snake was in the [Summer League/Veteran Division](https://play.battlesnake.com/competitions/summer-league/). Still active on the global arena. Based on the Alpha snake, but fewer bugs and a bit quicker.  Decent snake using minimax/payoff matrix algorithm only. This snake can play standard, squad, and royale.
* Gamma : This snake was in the Fall League and in [Winter Classic](https://play.battlesnake.com/competitions/winter-classic-2020/) in elite division. Based on Beta snake, but with some area control features. With the new release Gamma is now more duel oriented. Doesn't take hazard sauce into account.


## Properties files

Each snake has a properties file. You can edit it with any text editor. If you change the file, you need to restart the snake.
Most of the basic properties are self-explanatory, but the `minusbuffer` property is a millisecond property to compensate for the latency. For example, if the timeout is 500ms and the minusbuffer is 150ms, then the snake will use 350ms.
Please take note that sometimes (maybe cause by Java's garbage collection) my snakes may timeout.

## How-to

To run a snake, you need Java installed  (any recent version).
In the command line, type `java -jar snake.jar <SnakeName>` e.g. `java -jar snake.jar Beta`

For Alpha, Beta and Gamma, you may add memory config, e.g. `java  -Xmx1024m -Xms1024m -jar snake.jar Beta`

The snake will listen on the port number from the `.properties` file.


# Release Notes

## 2021-03-09   New release
* Gamma and Beta are now multithreaded.
* Fixed the issue where Gamma/Beta weren't able to play on a non-square board.
* Improve Gamma's area control algorithm
* Few performance adjustments.
