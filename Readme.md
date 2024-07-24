# Sudoku Solver

A simple Java-based application to solve a 9x9 Sudoku puzzle. The program uses a backtracking algorithm to find the solution, filling in the puzzle with numbers from 1 to 9 while respecting the rules of Sudoku.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [How It Works](#how-it-works)
- [Code Structure](#code-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

This Sudoku Solver application solves a given Sudoku puzzle using a backtracking algorithm. The program fills in the puzzle with numbers from 1 to 9 while ensuring that each number appears only once per row, column, and 3x3 sub-grid.

## Features

- **Backtracking Algorithm:** Efficiently solves the Sudoku puzzle.
- **Input Flexibility:** Can be adapted to take different puzzle inputs.
- **Output Display:** Prints the solved puzzle to the console.

## How It Works

1. **Board Representation:** The Sudoku board is represented as a 2D array of integers. Zeros in the array represent empty cells.
2. **Backtracking:** The solver iteratively tries numbers from 1 to 9 in each empty cell. If a valid number is found (i.e., it doesn't violate Sudoku rules), it is placed in the cell. The process continues recursively for the next empty cell.
3. **Validation:** The `isValid` method checks whether placing a number in a cell follows Sudoku rules.
4. **Completion:** If the entire board is filled without conflicts, the puzzle is solved; otherwise, the solver backtracks to find a different solution path.

## Code Structure

### `SudokuSolver.java`

- **Main Method:**
  - Initializes the Sudoku board with a sample puzzle.
  - Calls `solveSudoku` to attempt solving the puzzle.
  - Prints the solved puzzle or indicates if the puzzle is unsolvable.

- **`solveSudoku(int[][] board)` Method:**
  - Iterates through the board to find empty cells.
  - Tries numbers 1-9 in each empty cell.
  - Recursively solves the board or backtracks if a number doesn't lead to a solution.

- **`isValid(int[][] board, int row, int col, int num)` Method:**
  - Checks the validity of placing `num` in the specified `row` and `col`.
  - Ensures no duplicate numbers in the row, column, and 3x3 sub-grid.

- **`printBoard(int[][] board)` Method:**
  - Prints the Sudoku board in a formatted manner.

## Installation

1. **Clone the repository:**
```bash
   git clone https://github.com/yourusername/sudoku-solver.git
   cd sudoku-solver
```

2. Compile the Java files:
``` bash
javac SudokuSolver.java
```
3. Run the application:
``` bash
    java SudokuSolver
```

## Usage

The application will attempt to solve the hardcoded Sudoku puzzle defined in the `main` method. You can modify the `board` array in the `main` method to solve a different puzzle. The solved puzzle or a message indicating that the puzzle is unsolvable will be printed to the console.

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or inquiries, please contact [varshneyanurag691@gmail.com](mailto:varshneyanurag691@gmail.com]).
