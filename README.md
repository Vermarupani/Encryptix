# Encryptix
C++ internship project
// Number Guesssing Game
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    int number, guess, nguess = 0;
    srand(static_cast<unsigned int>(time(0)));
    number = rand() % 100 + 1;

    do {
        cout << "Guess the number between 1 and 100: ";
        cin >> guess;
        nguess++;

        if (guess > number) {
            cout << "Lower number please!" << endl;
        } else if (guess < number) {
            cout << "Higher number please!" << endl;
        } else {
            cout << "Congratulations! You guessed the number in " << nguess << " attempts." << endl;
        }
    } while (guess != number);

    return 0;
}
