# SudokuSolver
A c++  program using backtracking and recursion

Backtracking is a technique to solve problems where multiple choices are there and we don't know the correct choice and hence we solve problem with trial and error i.e. trying each option until goal is achieved.
Like all other Backtracking problems, we can solve Sudoku by one by one assigning numbers to empty cells. Before assigning a number, we check whether it is safe to assign. We basically check that the same number is not present in the current row, current column and current 3X3 subgrid. After checking for safety, we assign the number, and recursively check whether this assignment leads to a solution or not. If the assignment doesn’t lead to a solution, then we try next number for the current empty cell. And if none of the number (1 to 9) leads to a solution, we return false.

![](https://github.com/ASTHA193/SudokuSolver/blob/master/s.png)

## Algorithm
* Find row, col of an unassigned cell
  * If there is none, return true
  * For digits from 1 to 9
    a) If there is no conflict for digit at row, col <br />
        assign digit to row, col and recursively try fill in rest of grid <br />
    b) If recursion successful, return true <br />
    c) Else, remove digit and try another <br />
  * If all digits have been tried and nothing worked, return false
