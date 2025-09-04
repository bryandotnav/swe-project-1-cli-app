# CLI Projects Assignment

- [Overview](#overview)
- [Assignment Goals](#assignment-goals)
- [Project Options](#project-options)
- [Technical Requirements (How This Project Will Be Assessed)](#technical-requirements-how-this-project-will-be-assessed)
  - [Core JavaScript Concepts (7 points)](#core-javascript-concepts-7-points)
  - [User Interaction (2 points)](#user-interaction-2-points)
  - [Code Organization (3 points)](#code-organization-3-points)
  - [Reflection Questions (3 points)](#reflection-questions-3-points)
- [Tips for Success](#tips-for-success)
- [Getting Started](#getting-started)
- [Setup Instructions](#setup-instructions)
- [🎮 Project 1: Rock–Paper–Scissors CLI Game](#-project-1-rockpaperscissors-cli-game)
  - [Key Features to Implement:](#key-features-to-implement)
  - [Data Structure](#data-structure)
  - [Stretch Features to Consider:](#stretch-features-to-consider)
- [🛒 Project 2: Shopping List CLI App](#-project-2-shopping-list-cli-app)
  - [Key Features to Implement:](#key-features-to-implement-1)
  - [Data Structure](#data-structure-1)
  - [Stretch Features to Consider:](#stretch-features-to-consider-1)
- [🧠 Project 3: Quiz Game CLI](#-project-3-quiz-game-cli)
  - [Key Features to Implement:](#key-features-to-implement-2)
  - [Data Structure](#data-structure-2)
  - [Stretch Features to Consider:](#stretch-features-to-consider-2)

## Overview

Your task is to create an interactive command-line application using Node.js. This project will demonstrate your understanding of fundamental JavaScript concepts and your ability to organize code into a well-structured application.

## Assignment Goals

You'll build a CLI application that users can interact with through their terminal. Your project should be something you can complete in just a few days while showcasing the core programming concepts we've covered.

## Project Options

Choose **one** of the following three projects to complete. They are ordered by difficulty, so pick the one that matches your comfort level and goals:

**🎮 Project 1: Rock–Paper–Scissors**
Build a classic game where users play against the computer with score tracking across multiple rounds.

**🛒 Project 2: Shopping List Manager**
Create a CRUD application where users can add, remove, and view items in their shopping list through a menu system.

**🧠 Project 3: Quiz Game**
Develop a multiple-choice quiz application with questions, scoring, and replay functionality.

## Technical Requirements (How This Project Will Be Assessed)

Your completed project will be assessed on the following criteria:

### Core JavaScript Concepts (7 points)
- **Variables**: Use clear, descriptive names that explain what data they hold
- **Functions**: Break your code into multiple functions that each handle specific tasks
- **Conditionals**: Include at least one `if/else` statement that changes behavior based on user input
- **Loops**: Use at least one `while` loop to repeatedly prompt the user
- **String Methods**: Use string methods (like `.toLowerCase()`, `.trim()`, etc.) to validate user input
- **Higher Order Array Methods**: Use at least one array higher-order method (like `.forEach()`, `.filter()`, `.reduce()`, etc...)
- **Objects**: Use at least one object to organize related data together

### User Interaction (2 points)
- Create an interactive experience that responds to user choices using the `prompt-sync` package
- Handle invalid input gracefully (inform the user of their mistake and let them try again)

### Code Organization (3 points)
- Split your code into **at least 3 separate modules** (files)
- Use `require()` and `module.exports` to connect your modules
- Follow a logical file structure:
  - `index.js` — the entry point of the application that displays a menu to the user.
  - `menu.js` — handles the main menu loop and handles user input.
  - Data Layer (choose a name!) — handles the logic related to managing the data for your application.

### Reflection Questions (3 points)
- In `reflection.md`, respond to the following prompts:
  1. Share one aspect of building this project you found challenging and how you overcame it.
  2. This project required you to separate your code into modules and into functions. Did this assist your project-building or slow you down? Explain?
  3. Share one technical concept that you gained a deeper understanding of through building this project. Explain that concept in simple terms and explain how it is used in your project.

## Tips for Success

- **Start Simple**: Get basic functionality working first, then add features
- **Test Frequently**: Run your code often to catch issues early
- **Plan Your Functions**: Think about what each function should do before coding
- **Handle Edge Cases**: What happens if a user enters invalid input?
- **Be Creative**: Add your own questions, features, or improvements!
- **Use Meaningful Names**: Your variable and function names should explain their purpose

## Getting Started

1. Choose your project based on your comfort level
2. Follow the setup instructions below
3. Plan out your functions and data structures
4. Start coding incrementally
5. Test and debug as you go

*Remember: The goal is to demonstrate your understanding of JavaScript fundamentals while building something functional and fun!*

## Setup Instructions

_Complete these steps after you have chosen your project!_

1. Create a new folder with a descriptive name for your project.
2. Run `npm init -y`.
3. Install `prompt-sync` with `npm install prompt-sync`.
4. Begin Coding!

## 🎮 Project 1: Rock–Paper–Scissors CLI Game

**Objective:**
Build a simple Rock–Paper–Scissors game where the user plays against the computer. The program should keep score across multiple rounds until the player decides to quit.

### Key Features to Implement:

* When a user starts the application, they are greeted with a nice message and is presented with a menu of options.
* The user can enter a number, 1 through 3, to select their next action:
  ```
  Menu:
  1. Play Round
  2. View Stats  
  3. Exit

  Choose an Action (Enter 1-3)
  ```
* When playing, the user can select their choice by typing "rock", "paper", or "scissors" (case-insensitive).
  * The computer randomly selects its choice.
  * The game compares the choices and determines the winner based on standard Rock-Paper-Scissors rules.
  * After each round, the game displays the choices made and the result
    ```
    You chose: rock
    Computer chose: scissors
    Rock beats scissors! You win!
    ```
* When viewing stats, the user can see games won, games lost, games tied, total games played, and win rate as a rounded percentage.
  ```
  Current Statistics:
  Games Won: 2
  Games Lost: 1
  Games Tied: 0
  Total Games: 3
  Win Rate: 67%
  ```
* The game continues until the user chooses to quit, then displays final statistics.


### Data Structure

Use an **object** to store game data. The object should look like this:

```js
{
  wins: 2,
  losses: 3,
  ties: 1
}
```

### Stretch Features to Consider:

* Add a "best of X rounds" mode where the game continues until someone wins a certain number of rounds
* Add sound effects or ASCII art for different choices (rock, paper, scissors)
* Track and display win streaks and longest winning/losing streaks
* Allow saving/loading game statistics to/from a JSON file using the `fs` module

## 🛒 Project 2: Shopping List CLI App

**Objective:**
Create a CLI shopping list manager where users can add, remove, and view items through a menu system.

### Key Features to Implement:

* When a user starts the application, they are greeted with a nice message and are presented with a menu of options.
* The user can enter a number, 1 through 4, to select their next action.
  ```
  Menu:
  1. Add Item
  2. Remove Item  
  3. View List
  4. Exit

  Choose an Action (Enter 1-4):
  ```
* When adding an item to the list, the user can specify the `name` of the item, the `quantity`, and the `price`.
  ```
  Enter item name: apples
  Enter quantity: 5
  Enter price per item: 0.50
  Added 5 apples at $0.50 each to your shopping list!
  ```
* When removing an item from the list, the user can specify the `name` of the item (case insensitive) and the `quantity` to remove.
  ```
  Enter item name to remove: apples
  Enter quantity to remove: 2
  Removed 2 apples from your shopping list!
  ```
* When viewing the list, the user can see the total quantity of items in the list and the total price.
  ```
  Your Shopping List:
  - 3 apples: $1.50
  - 2 bread: $4.00
  - 1 milk: $3.50
  
  Total Items: 6
  Total Price: $9.00
  ```
* After selecting an action, the application displays a message to confirm the completion of their action.
* After selecting an action, the menu is shown again to the user and they are prompted to choose their next action.

### Data Structure

Use an **array of objects** to store shopping items. Each item should be an object like this: 

```js
{
  name: "apples",
  quantity: 3,
  price: 1.5
}
```

### Stretch Features to Consider:

* Add an option to sort. Let the user choose between `price`, `quantity`, and `name`
* Add a `category` to each item and add it as an option for sorting
* Add a budget feature that warns when total cart value exceeds a set amount
* Allow saving/loading shopping lists to/from a JSON file using the `fs` module
* Add a "shopping mode" that lets users check off items as they shop
* Add support for multiple shopping lists (e.g., groceries, hardware, gifts)

## 🧠 Project 3: Quiz Game CLI

**Objective:**
Build a multiple-choice quiz game where users answer questions, get feedback, and see their score at the end.

### Key Features to Implement:

* When a user starts the application, they are greeted with a nice message and presented with a menu of options.
* The user can enter a number, 1 through 3, to select their next action.
  ```
  Menu:
  1. Start Quiz
  2. View High Scores
  3. Exit

  Choose an Action (Enter 1-3)
  ```
* When starting a quiz, the application presents questions one at a time with multiple choice options.
* Each question displays the question text and numbered choices for the user to select from. For example:
  
    ```
    Question 1: What is 2 + 2?
    1) 3
    2) 4
    3) 5
    4) 6
    
    Enter your answer (1-4): 
    ```

* After answering each question, the user receives immediate feedback on whether their answer was correct.
  ```
  Correct! Well done!
  Current Score: 2/3 (67%)
  ```
* At the end of the quiz, the user sees their final score and percentage (rounded) of correct answers.
  ```
  Quiz Complete!
  Final Score: 4/5 (80%)
  Thanks for playing!
  ```

* When viewing high scores, users can see the top 5 scores and a `Date` timestamp when the quiz was completed.
* After completing an action, the menu is shown again and the user is prompted to choose their next action.

### Data Structure

Use an **array of objects** to store quiz questions. Each question should be an object like this: 

```js
{
  question: "What is 2+2",
  choices: ["3", "4", "5", "6"],
  answerIndex: 1
}
```

### Stretch Features to Consider:

* Add different categories of questions (math, science, history, etc.) and let users choose their preferred category
* Implement a difficulty system with easy, medium, and hard questions
* Add a timer for each question to create a more challenging experience
* Allow saving/loading quiz results and high scores to/from a JSON file using the `fs` module