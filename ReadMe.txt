Xizhe Sun



Sample execution:
Enter the row 0 : 5 3 0 0 7 0 0 0 0
Enter the row 1 : 6 0 0 1 9 5 0 0 0
Enter the row 2 : 0 9 8 0 0 0 0 6 0
Enter the row 3 : 8 0 0 0 6 0 0 0 3
Enter the row 4 : 4 0 0 8 0 3 0 0 1
Enter the row 5 : 7 0 0 0 2 0 0 0 6
Enter the row 6 : 0 6 0 0 0 0 2 8 0
Enter the row 7 : 0 0 0 4 1 9 0 0 5
Enter the row 8 : 0 0 0 0 8 0 0 7 9 
 -----------------------
| 5 3 4 | 6 7 8 | 9 1 2 | 
| 6 7 2 | 1 9 5 | 3 4 8 | 
| 1 9 8 | 3 4 2 | 5 6 7 | 
 -----------------------
| 8 5 9 | 7 6 1 | 4 2 3 | 
| 4 2 6 | 8 5 3 | 7 9 1 | 
| 7 1 3 | 9 2 4 | 8 5 6 | 
 -----------------------
| 9 6 1 | 5 3 7 | 2 8 4 | 
| 2 8 7 | 4 1 9 | 6 3 5 | 
| 3 4 5 | 2 8 6 | 1 7 9 | 
 -----------------------
Runtime complexity is O(n^3):

In the code I have nested for loop at the top:
for (int j = 0; j < 9; j++) {
	for (int i = 0; i < 9; i++) {
		if (board[i][j] == 0) {
			x = i;
			y = j;
			break;
		}
	}
} its complexity is O(n*n), followed by another for loop at bottom:
for (int k = 1; k < 10; k++) {
...
that has recursive call.
Therefore, big O of nested for loop plus big O of second for loop is equal to big O of nested loop.
and since this is a recursion function, by looking at the for loop at the bottom, the recursion can be repeated n times
therefore the big O of the algorithm is O(n*n*n) = O(n^3)

space complexity O(n^2):

Two dimensional array is used to store the solution each array of size n
