Download Link: https://assignmentchef.com/product/solved-cs3610-project-3
<br>
For this project, you will write a recursive backtracking program to solve the knight’s tour problem as described in exercise 19 on page 393 of your textbook “Data Structures Using C++”. You have been provided template code that you must modify to complete this assignment. Specifically, you will implement the following two functions:

void KnightsTour::move(int row, int col, int&amp; m, int&amp; num tours) : move is a recursive backtracking function that will print all solutions to the knight’s tour problem on a chessboard starting from positions row, col. The total number of tours found is returned in the reference variable num tours.

In this function, m is an integer that represents the current move of the tour (moves are labeled starting from 1). It is incremented at the beginning of each call to move to indicate at what point along the tour the knight reached the chessboard cell at indices row, col. In each call to move, you will record the value of m in the private member variable board at position row, col. Next, you will find all valid knight moves reachable from position row, col using the function get moves. For each new move found from get moves, recursively call move to find all remaining tours.

When m equals the total number of cells in the private member variable board, it means a tour has been completed. Every time a tour has completed, you will print board using the provided function print.

void KnightsTour::get moves(

int row, int col, int row moves[], int col moves[], int&amp; nummoves

) :

get moves is used to find all valid knight moves reachable from board indices row, col. An invalid move would be one that sends the knight off the edge of the board or to a position that has already been visited in the tour.

row moves and col moves are arrays used to store the indices of all new valid moves found. num moves is used to indicate how many valid moves were found.

In other words, num moves records the sizes of row moves and col moves.

To ensure that everyone’s output remains consistent with the test cases used in grading, check all valid moves in a CLOCKWISE FASHION starting from the move in which the knight travels two squares to the right and one square up.

In this project, your are only required to find tours on a 5×5 chessboard starting at locations specified by the user. The driver program to setup this chessboard and accept user input has already been provided. There is no need to modify it.

<h1>Input</h1>

Find all knight’s tours for a 5×5 chessboard starting from indices 0 ≤ <em>r &lt; </em>5 and 0 ≤ <em>c &lt; </em>5. <em>r </em>and <em>c </em>are to be passed in as command line arguments. (A driver program has already been implemented for you).

<h1>Output</h1>

Print the solution for every knight’s tour found starting from position <em>r, c </em>along with the total number of tours <em>t</em>. (Remember to call print inside move).

<h1>Sample Test Cases</h1>

<strong>Test Case 1</strong>

<table width="586">

 <tbody>

  <tr>

   <td width="586">$ ./a.out 3 323        4      11            16 2512         17 24                5 103 22 9 18 15 8 13 20 1 621        2           7 14         1921        4      11            16 1912         17 20                5 103 22 9 18 15 8 13 24 1 623        2           7 14         25…21      14        3        8      234 9 22 13 2 17 20 15 24 7 10 5 18 1 1219         16 11                6 25Number of tours: 56</td>

  </tr>

 </tbody>

</table>