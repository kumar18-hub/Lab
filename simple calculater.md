#include <iostream>
using namespace std;

void showMenu() {
    cout << "\nSimple Calculator\n";
    cout << "1. Addition (+)\n";
    cout << "2. Subtraction (-)\n";
    cout << "3. Multiplication (*)\n";
    cout << "4. Division (/)\n";
    cout << "Choose an operation (1-4): ";
}

void calculator() {
    double num1, num2, result;
    int choice;

    showMenu();
    cin >> choice;

    cout << "Enter first number: ";
    cin >> num1;
    cout << "Enter second number: ";
    cin >> num2;

    switch (choice) {
        case 1: result = num1 + num2; break;
        case 2: result = num1 - num2; break;
        case 3: result = num1 * num2; break;
        case 4:
            if (num2 != 0) result = num1 / num2;
            else {
                cout << "Error: Division by zero is not allowed.\n";
                return;
            }
            break;
        default:
            cout << "Invalid choice.\n";
            return;
    }

    cout << "Result = " << result << endl;
}
