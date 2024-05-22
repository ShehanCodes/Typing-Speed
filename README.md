# Typing Speed Test Program

This Typing Speed Test program is a terminal-based application that helps users measure their typing speed in words per minute (WPM). It uses the `curses` library to create an interactive user interface within the terminal.

## Features

- **Interactive Typing Test:** Users type a randomly selected line of text and their typing speed is calculated in real-time.
- **Real-time WPM Calculation:** The program displays the user's current typing speed in words per minute.
- **Accuracy Feedback:** Characters typed correctly are displayed in green, while incorrect characters are displayed in red.

## Prerequisites

- Python 3.x
- `curses` library (standard library for Unix-based systems)

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/typing-speed-test.git
    cd typing-speed-test
    ```

2. **Prepare the text file:**
    - Ensure you have a `text.txt` file in the same directory as the script. This file should contain lines of text, each line representing a different typing test entry.

## Usage

1. **Run the program:**
    ```sh
    python typing_speed_test.py
    ```

2. **Instructions:**
    - When you start the program, you'll see a welcome message. Press any key to begin the test.
    - Type the displayed text as accurately and quickly as you can.
    - Your WPM will be displayed as you type.
    - If you complete the text, a message will appear indicating you have finished. Press any key to continue or `ESC` to exit.

## Code Overview

- **`start_screen(stdscr)`:** Displays the initial screen prompting the user to start the test.
- **`display_text(stdscr, target, current, wpm=0)`:** Displays the target text, current user input, and the WPM count.
- **`load_text()`:** Loads a random line of text from `text.txt`.
- **`wpm_test(stdscr)`:** Manages the main typing test logic, calculating WPM and handling user input.
- **`main(stdscr)`:** Initializes the curses color pairs and starts the typing test.

## Example

Here's a simple example of what the interaction might look like:

```text
Are you ready to test your typing speed?
Press any key to start the test!

The quick brown fox jumps over the lazy dog.
WPM: 45

Well Done! You completed the test! Press any key to continue.
