#include <iostream>

#include <time.h>       // time 

using namespace std;

int start(){

  cout << "Welcome to the number guessing game!" << endl;
  bool start = true;
  int secret, guess;
  int count = 0;

  // initialize random seed
  srand(time(NULL));

  // generate secret number between 0 and 100
  secret =  rand() % (100 + 1 - 0) + 0;
  
  //run this loop while the game is in action
  while (start == true){

    cout << "Guess the number between 0 - 100: " << endl;
    cin >> guess;
      //if the guess is correct, then player won't guess again, else it continues to guess
    // adding to the guess count, while determining if the guess is too high or low
      if (guess == secret)
      {
        cout << "Yay! You guess correctly!" << endl;
        cout << "You guessed " << count << " times." << endl;
        start = false;
      }
      else if (guess > secret) 
      {
        cout << "Your guess is too high. Guess again." << endl;
        count++;
      }
      else if (guess < secret)
      {
        cout << "Your guess is too low. Guess again." << endl;
        count++;
      }
    }
  return 0;
  }


int main()
{
  char answer;
  bool valid = true;
  start();
//while the input of the user is valid run this loop
  while (valid == true) {
    cout << "Would you like to play again? Type y for yes or n for no." << endl;
    cin >> answer;
    //if the user inputs y, rerun the game, if not end
    if (answer == 'y')
    {
      start();
    }
    else if (answer == 'n') 
    {
      cout << "Thanks for playing! :)" << endl;
      valid = false;
    }
    else {
      cout << "Invalid input. Would you like to play again? Type y for yes or n for no." << endl;
    }
  } 
 return 0;
}
	
