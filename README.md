# Rasta-RiskRoom-MiniGame

This repository contains the source code for a quiz game developed for the Rasta Summer School 2022. The game is built using Python and Tkinter for the graphical user interface. Players answer a series of questions, and based on their answers, they have a chance of winning with odds ranging from 20% to 70%.

## Features
- Multiple choice questions
- Dynamic odds calculation based on answers
- Graphical user interface using Tkinter

## How to Play
- The game presents a series of multiple-choice questions.
- Select the correct answer by clicking on the choice.
- A wrong answer ends the game.
- After each correct answer, the player can choose to continue or end the game.
- The winning chance increases with each correct answer, up to a maximum of 70%.
- If the player chooses to end the game, a random draw determines if they win based on their accumulated odds.

## Code Walkthrough

### Main Structure
- The game is initialized in the `__main__` block, where the main window and game logic are set up.
- `Question` class: Represents a quiz question, with the question text, choices, and the index of the right choice.

### Game Logic
- Questions are randomly shuffled and presented one by one.
- The `handle_click` function manages the player's answers.
- The game calculates the chance of winning after each correct answer.
- If the player chooses to continue after a question, the game progresses to the next question; otherwise, the final draw occurs.

### GUI Components
- Tkinter is used to create the graphical interface.
- Questions and choices are displayed in labels and buttons.
- Message boxes are used for showing win/lose information and asking whether to continue.

### Randomness and Odds Calculation
- The `random` library is used to shuffle questions and calculate the winning odds.
- The winning chance starts at 1/3 and increases with each correct answer, with a cap of 70%.
