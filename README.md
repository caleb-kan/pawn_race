# Kotlin Pawn Race Autorunner

Here lies the home of the Kotlin Pawn Race autorunner. This handy little jar will allow you to run your pawnrace
code against either the autorunner's random AI, itself, or another students/another version of your solution 
(if you have the `pawnrace.jar`).

## Instructions
To use the jar, first ensure that the `pawnrace.jar` file you want to run is contained within a folder
called `kotlinpawnrace_YOURUSERNAME`. Handily, if you followed the spec, you'll have cloned your repo into
this folder, and your username will be used as the player name: so just build a _runnable_ jar and play away!

To run the autorunner, you can use one of three different methods:

### Running against the random AI
To run your code against the autorunner's prebuilt solution, you can use the following command:

```
> java -jar -ea pawnrace-autorunner.jar 0 kotlinpawnrace_USERNAME
```

Be sure to replace `USERNAME` with your actual username. By passing 0 to the autorunner, you instruct it to
play a single game using its own AI. It will pick which colour you are assigned at random

### Running against yourself
To run your AI against itself, you can use the following command:

```
> java -jar -ea pawnrace-autorunner.jar N kotlinpawnrace_USERNAME
```

Again, replace `USERNAME` with your own username, and `N` with the number of games you want to play (up to 58
, at which point you run out of playable gaps). The autorunner will again assign each instance of your AI
with a random colour. It is worth nothing that, in addition to this, you may also write:

```
> java -jar -ea pawnrace_autorunner.jar N kotlinpawnrace_USERNAME kotlinpawnrace_USERNAME
```

This has the same effect.

### Running against another solution
To run the AI against a different solution (another students AI, or perhaps an alternative one you have produced),
first collect the `pawnrace.jar`, and place it in a folder called `kotlinpawnrace_THEIRPLAYERNAME`, replacing 
`THEIRPLAYERNAME` with a name which identifies them for the autorunner. This should folder should be in the 
same folder as the `pawnrace_autorunner.jar` (i.e. this one). Then you can run it with the familiar:

```
> java -jar -ea pawnrace_autorunner.jar N kotlinpawnrace_PLAYER1 kotlinpawnrace_PLAYER2
```

You should, again, replace `PLAYER1` and `2` with the names of the folders themselves. The autorunner will play
then off against eachother for N rounds, and will assign colours randomly for the first game, and swap every
subsequent game.

Have fun!

## Other Flags
The autorunner supports some additional flags to control the output. Currently, one of the two following flags may
be used as the *first* argument to the autorunner (or neither of them):

* `--invert-colours`: This can be used to switch over the unicode characters used to print on the terminal if
  your terminals font colour is inverted
* `--ascii-colours`: This can be used to turn off unicode piece printing and instead use `W` and `B` to represent
  the pieces
