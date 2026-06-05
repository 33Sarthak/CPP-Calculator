 

#include <iostream>
using namespace std;

// Functions

double add(double a, double b)
{
    return a + b;
}

double subtractNumbers(double a, double b)
{
    return a - b;
}

double multiplyNumbers(double a, double b)
{
    return a * b;
}

double divideNumbers(double a, double b)
{
    return a / b;
}

int modulusNumbers(int a, int b)
{
    return a % b;
}

double squareNumber(double a)
{
    return a * a;
}

int main()
{
    int choice;

    while(true)
    {
        cout << "\n===== CALCULATOR =====\n";
        cout << "1. Add\n";
        cout << "2. Subtract\n";
        cout << "3. Multiply\n";
        cout << "4. Divide\n";
        cout << "5. Exit\n";
        cout << "6. Modulus\n";
        cout << "7. Square\n";

        cout << "\nEnter Choice: ";
        cin >> choice;

        if(choice == 5)
        {
            cout << "Thank you for using Calculator!\n";
            return 0;
        }

        switch(choice)
        {
            case 1:
            {
                double a, b;
                cout << "Enter first number: ";
                cin >> a;
                cout << "Enter second number: ";
                cin >> b;

                cout << "Result = " << add(a, b) << endl;
                break;
            }

            case 2:
            {
                double a, b;
                cout << "Enter first number: ";
                cin >> a;
                cout << "Enter second number: ";
                cin >> b;

                cout << "Result = " << subtractNumbers(a, b) << endl;
                break;
            }

            case 3:
            {
                double a, b;
                cout << "Enter first number: ";
                cin >> a;
                cout << "Enter second number: ";
                cin >> b;

                cout << "Result = " << multiplyNumbers(a, b) << endl;
                break;
            }

            case 4:
            {
                double a, b;

                cout << "Enter first number: ";
                cin >> a;

                cout << "Enter second number: ";
                cin >> b;

                if(b == 0)
                {
                    cout << "Cannot divide by zero!\n";
                }
                else
                {
                    cout << "Result = " << divideNumbers(a, b) << endl;
                }
                break;
            }

            case 6:
            {
                int a, b;

                cout << "Enter first integer: ";
                cin >> a;

                cout << "Enter second integer: ";
                cin >> b;

                if(b == 0)
                {
                    cout << "Cannot perform modulus by zero!\n";
                }
                else
                {
                    cout << "Result = " << modulusNumbers(a, b) << endl;
                }

                break;
            }

            case 7:
            {
                double a;

                cout << "Enter a number: ";
                cin >> a;

                cout << "Result = " << squareNumber(a) << endl;
                break;
            }

            default:
            {
                cout << "Invalid Choice!\n";
            }
        }
    }

    return 0;
}
