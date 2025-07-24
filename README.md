# 🧩 Sudoku Solver (C++)

## 📌 Project Overview

This is a **terminal-based Sudoku Solver**, written in C++, that takes in Sudoku puzzles (either manually or from a file) and solves them using **recursive backtracking**. It also provides a nicely formatted terminal UI for grid display and tracks the number of recursive calls made during the solving process.

---

## ✨ Features

* ✅ User can input Sudoku puzzle manually or via a file
* 🔁 Solves puzzles using recursive backtracking
* 🔍 Validates every move against Sudoku rules (row, column, 3×3 grid)
* 📊 Displays recursion statistics
* 🎨 Outputs a color-coded visual of the grid (if supported)
* 💥 Error handling for invalid puzzle inputs

---

## 🛠️ How It Works

### ➕ Input Options

On running the program, the user is prompted to:

1. **Enter values manually** (0 for empty cells), or
2. **Read from a file** containing 81 space-separated integers.

### 🔢 Solving Logic

* Uses **recursive backtracking** to explore possible values for each empty cell.
* Checks for validity:

  * No duplicates in the same row
  * No duplicates in the same column
  * No duplicates in the 3×3 subgrid

### 📈 Stats

* Tracks number of recursive function calls
* Displays a message whether the puzzle was solved or not

---

## 🧪 Example File Format

Example `puzzle.txt`:

```
5 3 0 0 7 0 0 0 0
6 0 0 1 9 5 0 0 0
0 9 8 0 0 0 0 6 0
8 0 0 0 6 0 0 0 3
4 0 0 8 0 3 0 0 1
7 0 0 0 2 0 0 0 6
0 6 0 0 0 0 2 8 0
0 0 0 4 1 9 0 0 5
0 0 0 0 8 0 0 7 9
```

---

## 📁 File Structure

```
.
├── SudokuSolver.cpp     # Main program file
├── puzzle.txt           # (Optional) Sudoku puzzle input file
└── README.md            # Project documentation
```

---

## 🧰 Requirements

* Windows OS (uses `<Windows.h>`)
* C++ Compiler (e.g., g++ on MinGW or MSVC)

### ⬇️ Compilation

Using g++:

```bash
g++ -o SudokuSolver SudokuSolver.cpp
```

### ▶️ Run

```bash
./SudokuSolver
```

---

## 🚨 Error Handling

* If the puzzle file contains a value outside `[0–9]`, the program exits with an error message.
* Validates user inputs for each cell.

---

## 📚 Key Classes

### `SudokuGrid`

* Handles reading input
* Provides methods like:

  * `setCellValue(row, col, value)`
  * `getCellValue(row, col)`
  * `displayGrid()`

### `SudokuSolver`

* Manages solving logic
* Validates individual cell values
* Tracks recursion stats

---

## 💡 Future Improvements

* Add GUI (e.g., using Qt)
* Support for puzzle difficulty levels
* Benchmark solver time for performance metrics

---
