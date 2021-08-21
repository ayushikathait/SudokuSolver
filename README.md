# Project_SUDOKU SOLVER


In this Project, we have to input a partially filled 9×9 2D array ‘grid[9][9]’, the goal is to assign digits (from 1 to 9) to the empty cells so that every row, column, and sub grid of size 3×3 contains unique digits from 1 to 9.
This Sudoku solution satisfies all of the following rules:
1.	Each of the digits 1-9 must occur exactly once in each row.
2.	Each of the digits 1-9 must occur exactly once in each column.
3.	Each of the digits 1-9 must occur exactly once in each of the 9 3x3 sub-boxes of the grid.
The '0' character indicates empty cells.

Basically, I have used backtracking algorithm to solve the Sudoku which is a type of brute force search. Backtracking is a depth-first search (in contrast to a breadth-first search), because it will completely explore one branch to a possible solution before moving to another branch. In this way, we can solve the Sudoku very easily.
Approach: 

Sudoku can be solved by one by one assigning numbers to empty cells. Before assigning a number, check whether it is safe to assign. Check that the same number is not present in the current row, current column and current 3X3 sub grid. After checking for safety, assign the number, and recursively check whether this assignment leads to a solution or not. If the assignment doesn’t lead to a solution, then try the next number for the current empty cell. And if none of the number (1 to 9) leads to a solution, return false and print no solution exists.

Complexity Analysis:  
•	Time complexity: O (9^ (n*n)). 
For every unassigned index, there are 9 possible options so the time complexity is O(9^ (n*n)). The time complexity remains the same but there will be some early pruning so the time taken will be much less than the naive algorithm but the upper bound time complexity remains the same.

•	Space Complexity: O (n*n). 
To store the output array a matrix is needed.

