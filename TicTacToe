#include <iostream>
#include <string>

using namespace std;

//initalize board and show functions
char board[3][3] = {{'-','-','-'}, {'-','-','-'}, {'-','-','-'}};
void printBoard();
void handle_turn(int &player);
char checkRows();
char checkColumns();
char checkDiagonals();
char checkWinner();
char checkTie(char board[][3]);
void resetBoard(char board[][3]);


int main() 
{
	//initalize variables
	bool stillGoing = true;
	bool inGame = true;
	bool validAnswer = false;
	string playAgain;
	int player = 1;
	string winner = " ";
	printBoard();

//while we are still in game (as in not told not to play again), and the game is still going then handle
	//the turn and check for winners and tie
	while (inGame == true) {
		while (stillGoing == true){
			handle_turn(player);
			if (checkWinner() == 'X' || checkWinner() == 'O'){
				stillGoing = false;
				winner = checkWinner();
			}
			else if (checkTie(board) == 'Y'){
				stillGoing = false;
				winner = "It's a tie! No one";
			}
		}
		//Print who won
		cout << winner << " won!" << endl;

		//ask if player wants to play again
		cout << "Play again? Please type Y or N." << endl;
		getline(cin, playAgain);
		validAnswer = false;

		//determine if a valid answer is given
		while (validAnswer == false) {
			// cout << "nish" << endl;
			if (playAgain == "y" || playAgain == "Y") {
				resetBoard(board);
				inGame = true;
				validAnswer = true;
				winner = " ";
				player = 1;
				stillGoing = true;
			}
			else if (playAgain == "n" || playAgain == "N") {
				inGame = false;
				validAnswer = true;
			}
			else {
				cout << "Invalid input, please re-enter: " << endl;
				cout << "Play again? Please type Y or N." << endl;
				getline(cin, playAgain);
			}
		}
	}
	//if not want to play again then leave
	cout << "Thanks for playing!" << endl;

}

//handle the player's turn
void handle_turn(int &player)
{
	string position;
	bool valid = false;
	char currentPlayer;
	bool input_valid = false;

	//assign player number to a letter
	if(player == 1)
	{
		currentPlayer = 'X';
	}
	else
	{
		currentPlayer = 'O';
	}
	
	//ask player to choose a posision and put that letter in the position
	while (valid == false) {
		cout << currentPlayer << "'s turn." << endl;
		cout << "Choose a position a1, a2, a3, b1, b2, b3, c1, c2, c3: " << endl;
		getline(cin, position); 

		while (input_valid == false) {
			if (position == "a1"|| position == "a2"|| position == "a3"|| position == "b1"|| 
						 position == "b2"|| position == "b3"|| position == "c1"|| position == "c2"|| position == "c3"){
				input_valid = true;
			}
			else {
				cout << "Invalid input. Choose a position a1, a2, a3, b1, b2, b3, c1, c2, c3: " << endl;
				getline(cin, position);
			//	cout << position << endl;
			}
		}

		if (position == "a1" && board[0][0] == '-')
		{
			board[0][0] = currentPlayer;
			valid = true;
		}
		else if (position == "a2" && board[0][1] == '-')
		{
			board[0][1] = currentPlayer;
			valid = true;
		}
		else if(position == "a3" && board[0][2] == '-')
		{
			board[0][2] = currentPlayer;
			valid = true;
		}
		else if(position == "b1" && board[1][0] == '-')
		{
			board[1][0] = currentPlayer;
			valid = true;
		}
		else if(position == "b2" && board[1][1] == '-')
		{
			board[1][1] = currentPlayer;
			valid = true;
		}
		else if(position == "b3" && board[1][2] =='-')
		{
			board[1][2] = currentPlayer;
			valid = true;
		}
		else if(position == "c1" && board[2][0] == '-')
		{
			board[2][0] = currentPlayer;
			valid = true;
		}
		else if(position == "c2" && board[2][1] == '-')
		{
			board[2][1] = currentPlayer;
			valid = true;
		}
		else if(position == "c3" && board[2][2] == '-')
		{
			board[2][2] = currentPlayer;
			valid = true;
		}
		else {
			cout << "You can't go there! Please go again" << endl;
		}
	
		printBoard();
	}
	//change players
	if(player == 1)
	{
		player = 0;
	}
	else
	{
		player = 1;
	}
}

//sets the board
void printBoard() 
{
	cout << " " << "   " << "1" << "   "  << "2" << "   "  << "3" << endl;
	cout << "a" << " | " << board[0][0] << " | " << board[0][1] << " | " << board[0][2] << endl;
	cout << "b" << " | " << board[1][0] << " | " << board[1][1] << " | " << board[1][2] << endl;
	cout << "c" << " | " << board[2][0] << " | " << board[2][1] << " | " << board[2][2] << endl;
	return;
}

//checks each row to see if there is an empty slot or if there is a winner and return whether there is
char checkRows()
{
	char winner = ' ';
	if(board[0][0] == board[0][1] && board[0][0] == board[0][2] && board[0][0]!= '-')
	{
		winner = board[0][0];
	}
	else if(board[1][0] == board[1][1] && board[1][0] == board[1][2] && board[1][0] != '-')
	{
		winner = board[1][0];
	}
	else if(board[2][0] == board[2][1] && board[2][0] == board[2][2] && board[2][0] != '-')
	{
		winner = board[2][0];
	}
	else {
		winner = 'N';
	}
	return winner;
}

//checks each column to see if there is an empty slot or if there is a winner and return whether there is
char checkColumns()
{
	char winner = ' ';
	if(board[0][0] == board[1][0] && board[0][0] == board[2][0] && board[0][0]!= '-')
	{
		winner = board[0][0];
	}
	else if(board[0][1] == board[1][1] && board[0][1] == board[2][1] && board[0][1] != '-')
	{
		winner = board[0][1];
	}
	else if(board[0][2] == board[1][2] && board[0][2] == board[2][2] && board[0][2] != '-')
	{
		winner = board[0][2];
	}
	else {
		winner = 'N';
	}
	return winner;
}

//checks each diagonal to see if there is an empty slot or if there is a winner and return whether there is
char checkDiagonals()
{
	char winner = ' ';
	if(board[0][0] == board[1][1] && board[0][0] == board[2][2] && board[0][0]!= '-')
	{
		winner = board[0][0];
	}
	else if(board[2][0] == board[1][1] && board[2][0] == board[0][2] && board[2][0] != '-')
	{
		winner = board[2][0];
	}
	else {
		winner = 'N';
	}
	return winner;
}

//checiks if there is a winner in a diagonal, row, or column
char checkWinner() {
	char winner = ' ';
	char rowWinner = checkRows();
	char colWinner = checkColumns();
	char diagWinner = checkDiagonals();

	if(rowWinner == 'X' || rowWinner == 'O') {
		winner = rowWinner;
	}
	else if (colWinner == 'X' || colWinner == 'O') {
		winner = colWinner;
	}
	else if(diagWinner == 'X' || diagWinner == 'O') {
		winner = diagWinner;
	}
	else {
		winner = 'N';
	}
	return winner;
}

//checks for a tie
char checkTie(char board[3][3]) {
	int x = 0;
	int y = 0;
	char tie = ' ';

	for(int i = 0; i < 3; i++ ){
		for(int j = 0; j < 3; j++ ){
		   if(board[i][j] == '-' ){
			   x++;
		   }
		}
		if (x > 0) {
			tie = 'N';
		}
		else {
			tie = 'Y';
		}
	}
	return tie;
}

//resets board
void resetBoard(char board[][3]) {
	for(int i = 0; i < 3; i++ ){
		for(int j = 0; j < 3; j++ ){
		   board[i][j] = '-';
		}
	}
}
