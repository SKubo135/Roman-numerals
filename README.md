# Roman-numerals

/* ----------------------------------------------------------------------------
* Copyright &copy; 2016 Sara Kubo <sarakubo@csu.fullerton.edu>
* ------------------------------------------------------------------------- */

/**
* Convert numbers to Roman Numerals.
*/

#include<iostream>
#include<string>
using std :: cout;
using std :: cin;
using std :: endl;

int main() {

string roman;
int integer;
int piece;

cout << "Please enter an integer: " << endl;
  cin >> integer;
  
  if ((integer >= 4000) || (integer <= 0)) {
    cout << "invalid" << endl;
  }
  else {
    
    if (integer >= 1000) {
        piece = integer / 1000;
    
        for (int i = 1; i < piece; i++) {
          roman += 'M' ;
        }
    }
    integer % 1000;
  }
   
   if (integer >= 100) {
    piece = integer/100;
    
      if (piece == 9) {
        roman =+ "CM";
      }
      else if (piece >= 5) {
        roman += 'D';
        
        for (int i = 0 ; i < piece - 5 ; i++) {
          roman += 'C';
        }
      }
      else if ( piece == 4) {
        roman += "CD";
      }
      else if (piece >= 1) {
        for (int i = 0 ; i < piece ; i++)
        roman += 'C';
      }
    }
    integer % 100;
    
    
    
  }
  
  
  do {
    cout << "Would you like to convert another integer? (Y/N)" << endl;
    } while (choice == 'y' || choice == 'Y')
  

  cout << "--> " << roman << endl;

  return 0;

}
