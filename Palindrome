#include <iostream>
#include <cstring>
#include <ctype.h>

using namespace std;

int main()
{
  char str[81];
  char str2[81];
  char str3[81];
  
//Ask person to enter a palindrome and take in a character array no longer than 80 characters
  cout << "Enter a Palindrome, no more than 80 characters: " << endl;
  cin.get(str, 81);
  cin.get();
  int length = strlen(str);

  // cin.get(str2, 81);
  //cin.get();
  // if (strcmp(str, str2) == 0) {
  //} compare
  // if (strcpy(str, str2) == 0) {
  //}copy 

  //copy the input into str2
  int count = 0;
  for (int i = 0; i < length; i++) {
    if (str[i] != '\0' && str[i] != ' ' && ispunct(str[i]) == 0) {
      str2[count] = tolower(str[i]);
      count++;
    }
  }
  str2[count]='\0';
  //cout << str2 << endl;

  // reverse str2 into str3
  int counter = 0;
  for (int i = count-1; i > -1; i--) {
    if (str2[i] != '\0' && str2[i] != ' ' && ispunct(str2[i]) == 0) {
      str3[counter] = str2[i];
      counter++;
    }
  }
  //cout << str3 << endl;

  // compare the arrays to determine if they are palindromes
  if (strcmp(str2, str3) == 0) {
    cout << "Palindrome" << endl;
  }
  else if (strcmp(str2, str3) != 0){
    cout << "Not a Palindrome." << endl;
  }
  return 0;

}
