# Egui-chess

Rust version of salewski-chess, now with a plain egui user interface.

![Alt text](http://ssalewski.de/tmp/salewski_chess.png)

The Rust source code of the engine avoids the use of global variables and has some bug fixes and
improvements compared to the initial Nim version.

We now have a plain egui user interface, which allows to set time per move, select players, and rotate the board.
Playing human vs. human and engine auto-play is possible as well. And when the program is launched from terminal, we can
print the move list. Currently the program uses no separate thread for the engine, which means that the GUI
is blocked for a few seconds. For auto play, that is a bit ugly, but auto play is generally only for testing purpose.

Perhaps we will create a Xilem GUI at the end of this year, or we may extend this egui version a bit.

```
git clone https://github.com/stefansalewski/egui-chess.git
cd egui-chess
cargo run --release
```

