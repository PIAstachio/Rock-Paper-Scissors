#include <iostream>
#include <string>
using namespace std;

int main() {
   const int ROCK = 0;
   const int PAPER = 1;
   const int SCISSORS = 2;
   string player1;
   string player2;
   int numRounds;
   int p1, p2;
   int p1Win = 0;
   int p2Win = 0;

   int seed;
   cin >> seed;
   srand(seed);

   cin >> player1;
   cin >> player2;
   
   cin >> numRounds;
   
   while (numRounds < 1) {
      cout << "Rounds must be > 0" << endl;  
      cin >> numRounds;
   }
   
   cout << player1 << " vs " << player2 << " for " << numRounds << " rounds" << endl;
   
   for (int i = 0; i < numRounds; ++i) {
      p1 = rand() % 3;
      p2 = rand() % 3;
   
      while (p1 == p2) {
         cout << "Tie" << endl;
         
         p1 = rand() % 3;
         p2 = rand() % 3;
      }
         
      if ((p1 == 0 && p2 == 2) || (p1 == 1 && p2 == 0) || (p1 == 2 && p2 == 1)) {
         p1Win += 1;
         cout << player1 << " wins with ";
         
         if (p1 == ROCK) {
            cout << "rock" << endl;
         }
         else if (p1 == PAPER) {
            cout << "paper" << endl;
         }
         else if (p1 == SCISSORS) {
            cout << "scissors" << endl;
         }
      }
      
      else {
         p2Win += 1;
         cout << player2 << " wins with ";
      
         if (p2 == ROCK) {
            cout << "rock" << endl;
         }
         else if (p2 == PAPER) {
            cout << "paper" << endl;
         }
         else if (p2 == SCISSORS) {
            cout << "scissors" << endl;
         }
      }
   }
   
   cout << player1 << " wins " << p1Win << " and " << player2 << " wins " << p2Win << endl;

   return 0;

}
