# 🎶 Note-Based Maze Navigator (Verilog)

This project demonstrates a digital system built in Verilog that listens to audio input (via a microphone), determines the musical note being played (C, D, E, F...), and uses the detected notes to navigate a player through a visual maze.

## 🚀 Features

- Microphone input processing
- Frequency measurement and musical note detection
- Note-based filtering for signal stability
- Maze rendering via VGA (640x480)
- Navigation in the maze using notes:
  - `C` → Move Left
  - `D` → Move Right
  - `E` → Move Up
  - `F` → Move Down
- Visual feedback via 7-segment display and LED indicators

## 📷 Visual Output

- Blue square → Player
- Green cell → Start position
- Red cell → Goal
- Black cells → Walls
- Yellow background → Path

## 🛠️ Requirements

- FPGA board (e.g., Tang Nano 9K or similar)
- Microphone input capable of supplying 24-bit audio
- VGA-compatible display
- Verilog/SystemVerilog support
- 7-segment display, LEDs, GPIOs

## 📂 Files

- `lab_top.sv`: Main module combining sound processing, note detection, maze logic, and VGA rendering.
- `config.svh`: Parameter definitions (included via preprocessor).

## 🔍 How It Works

1. The module captures microphone audio data.
2. A zero-crossing counter measures the period of the waveform.
3. It maps the period to a musical note based on predefined frequencies.
4. The note is filtered to avoid glitches.
5. Based on the note detected, the player moves inside a hard-coded maze.
6. The maze and player are visualized on a VGA screen.

## 📈 Future Ideas

- Add dynamic maze generation
- Display current note name on the 7-segment display
- Add support for more musical notes and more complex commands
- Use UART to output note or position data
