you know what is a set ?
Right ?
Riiight....?

### What is the problem asking ?

- sudoku is represented as a 3x3 2d matrix 
- Each **row** and **column** should be unique 
	(should contain 0 - 9)
- squares should also be unique
- If any of the three conditions turn out to be False then return false else true

### algo:

```
row = defaultdict(set)
column = defaultdict(set)
square = defaultdict(set)
for i in range(9):
	for j in (9):
		if board[i][j] == '.':
			continue
		if (board[i][j]  in row[i] or 
		    board[i][j]  in coloumn[j] or 
		    board[i][j]  in square[i//3,j//3]):
				return False
		row[i].add(board[i][j])
		column[i].add(board[i][j])
		square[i//3,j//3].add(board[i][j])
		    
return True
```

we are just maintaining a set for each row, column and square
We used set because we are checking for uniqueness for each element that we are visiting
