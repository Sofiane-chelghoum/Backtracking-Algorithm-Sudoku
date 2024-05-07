# Backtracking Algorithm for Sudoku

## Introduction to Backtracking Algorithm

Backtracking is an effective algorithmic technique for solving problems by incrementally building a solution and backtracking when it hits a dead end. It systematically explores possible configurations while respecting the constraints of the problem. In the case of Sudoku, backtracking is utilized to fill in a partially completed grid with numbers from 1 to 9, ensuring that no row, column, or 3x3 subgrid contains duplicates.

![Backtracking Algorithm](images/Backtracking_Sudoku.png)

## Understanding the Sudoku Problem

Sudoku is a logic-based combinatorial number-placement puzzle. The objective is to fill a 9×9 grid with digits so that each column, each row, and each of the nine 3×3 subgrids that compose the grid contain all of the digits from 1 to 9.

![Sudoku Puzzle](images/Sudoku_Puzzle.png)

## Algorithm Steps

### Initialization

- Start with a partially filled Sudoku grid.

### Recursive Backtracking

1. **Base Case:** If the grid is filled completely (no empty cells), print the solution and return `True`.
2. **Find Empty Cell:** Locate the next empty cell (denoted by 0) in the grid.
3. **Try Numbers:** For each digit from 1 to 9, try placing it in the empty cell.
4. **Validation:** Check if the placement is valid according to Sudoku rules.
5. **Recursion:** If the placement is valid, recursively try to fill the remaining empty cells.
6. **Backtrack:** If no valid number can be placed, backtrack by undoing the current placement and trying the next digit.

## Code Structure

### `solveSudoku` Function

- **Input Parameters:**
  - `grid`: The Sudoku grid represented as a 2D array.
- **Output:**
  - Returns `True` if a solution is found, otherwise `False`.

### `isValid` Function

- **Input Parameters:**
  - `grid`: The Sudoku grid represented as a 2D array.
  - `row`: The current row.
  - `col`: The current column.
  - `num`: The number to be placed.
- **Output:**
  - Returns `True` if the placement is valid, otherwise `False`.

## How to Run the Code

1. **Download and Setup:**
   - Download the provided Python code containing the `solveSudoku` and `isValid` functions into a Python script file (e.g., `sudoku_solver.py`).

2. **Open a Text Editor:**
   - Use any text editor to open the downloaded Python script (`sudoku_solver.py`).

3. **Adjust the Sudoku Grid:**
   - Modify the initial Sudoku grid in the code to match the puzzle you want to solve. Use `0` to represent empty cells.

4. **Run the Script:**
   - Open a terminal or command prompt.
   - Navigate to the directory containing the Python script.
   - Execute the script by typing `python sudoku_solver.py` and pressing Enter.

The script will attempt to solve the Sudoku puzzle and print the solution if found. If no solution is found, it will indicate that the puzzle is unsolvable.

## Conclusion

This backtracking algorithm offers an efficient approach to solving Sudoku puzzles by systematically exploring potential solutions while adhering to the rules of the game. It demonstrates the power of recursion and backtracking in solving complex combinatorial problems.
