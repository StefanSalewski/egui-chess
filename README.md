# Egui Chess

## Deprecated

Please consider using [tiny-chess](https://github.com/StefanSalewski/tiny-chess) instead. The tiny-chess version executes the chess engine in a background thread, preventing the GUI from blocking. However, be aware that it has not been extensively tested yet and its code is slightly more complex.

In the future, we may remove this version or replace its engine with the extended one from tiny-chess.

![Chess UI](http://ssalewski.de/tmp/egui-chess.png)

This Rust version of salewski-chess features a basic `egui` user interface without threading support.

The Rust engine code avoids global variables and includes several bug fixes and improvements over the original Nim version.

### Features

- **User Interface**: The `egui` interface allows setting the time per move, selecting players, and rotating the board.
- **Game Modes**: Supports human vs. human gameplay and engine auto-play.
- **Move List**: When launched from the terminal, the program can print the move list.

### Current Limitations

This version does not use a separate thread for the engine, causing the GUI to block for a few seconds during computations. This can be inconvenient for auto-play, which is primarily intended for testing purposes.

### How to Run

```sh
git clone https://github.com/stefansalewski/egui-chess.git
cd egui-chess
cargo run --release
```

