

#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;



int main() {
   
	int player, computer;
	cout << "Take a value >>" << endl << "Rock = 0\n" << "Paper = 1\n" << "Scissor = 2\n";
	cin >> player;
	if (player < 0 || player > 2) {
		cout << "Not Valid Value" << endl;
		return 1;
	}
	srand(time(0));
	computer = rand() % 3;
	cout << "The Computer Takes : " << computer << endl;

	if (player == computer) {
		cout << "Draw" << endl;
	}

	else if ((player == 0 && computer == 2) || (player == 1 && computer == 0) || (player == 2 && computer == 1)) {
		cout << "You Win" << endl;
	}

	else {
		cout << "Computer Wins" << endl;
	}

	return 0;
}



