#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

void playGuessingGame() {
    srand(time(0));
    int number = rand() % 100 + 1;
    int guess;
    int attempts = 0;

    cout << "Welcome to the Number Guessing Game\n";
    cout << "Guess a number between 1 and 100\n";

    do {
        cout << "Enter your guess: ";
        cin >> guess;
        attempts++;

        if (guess > number) {
            cout << "Too high. Try again.\n";
        } else if (guess < number) {
            cout << "Too low. Try again.\n";
        } else {
            cout << "Correct! You guessed the number in " << attempts << " attempts.\n";
        }

    } while (guess != number);
}

int main() {
    playGuessingGame();
    return 0;
}
