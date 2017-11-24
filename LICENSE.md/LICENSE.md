#include<iostream>
#include<string>
#include<math.h>
using namespace std;

int sum(int x, int y) {
		return x + y ;
	}
int diff(int x, int y) {
		return x - y ;
	}
int product (int x, int y) {
		return x * y ;
}
int div (int x, int y) {
		return x / y ;
}
int remainder (int x, int y) {
		return x % y ;
}

main () {
float a, b, work, option, result, degrees;
char ans;

do {
cout << "Do you want to work with one or two numbers? " << endl << "Type (1) or (2)" << endl;
cin >> work;

if (work==1) {
	cout << "Enter your number: ";
	cin >> a;
	cout << "What do you want to make with that number?" << endl;
	cout << "Trigonometric Functions:" << endl;
	cout << "(1) Apply sin(" << a << ")" << endl;
	cout << "(2) Apply cos(" << a << ")" << endl;
	cout << "(3) Apply tan(" << a << ")" << endl;
	cout << "(4) Apply csc(" << a << ")" << endl;
	cout << "(5) Apply sec(" << a << ")" << endl;
	cout << "(6) Apply cot(" << a << ")" << endl;
	cout << "(7) Find Square Root" << endl;
	cout << "(8) Raise " << a << " to a power" << endl;

	cin >> option;

	if (option == 1 ){
		result = sin(a);
		cout << "sin(" << a << ") is equal to  " << result << " radians." << endl;
	} else if (option == 2){
		result = cos(a);
		cout << "cos(" << a << ") is equal to  " << result << " radians." << endl;
	} else if (option == 3) {
		result = tan(a);
		cout << "tan(" << a << ") is equal to  " << result << " radians." << endl;
	} else if (option == 4) {
		result = sin(1/a);
		cout << "csc(" << a << ") is equal to  " << result << " radians." << endl;
	} else if (option == 5) {
		result = cos(1/a);
		cout << "sec(" << a << ") is equal to  " << result << " radians." << endl;
	} else if (option == 6) {
		result = tan(1/a);
		cout << "cot(" << a << ") is equal to  " << result << " radians." << endl;
	} else if (option == 7) {
		result = sqrt(a);
		cout << "The squeare root of " << a << " is " << result << endl;
	} else if (option == 8) {
		cout << "Raise " << a << " to a power of: ";
		cin >> b;
		result = pow(a,b);
		cout << a << " raised to a power of " << b << " is equal to " << result << endl;
	}

} else {

  	cout << "Enter your first number: ";
  	cin >> a;
  	cout << "Enter your second number: ";
  	cin >> b;

  	cout << "What do you want to make with those numbers? " << endl;
  	cout << "(1) Add them" << endl << "(2) Substract them" << endl
  	<< "(3) Multiply them" << endl << "(4) Divide them" << endl
  	<< "(5) Get the remainder" << endl;
  	cin >> option;

  	if (option == 1 ){
    	cout << "The sum of " << a << " and " << b << " is " << sum(a,b) << endl;
  	} else if (option == 2) {
    	cout << "The diference of " << a << " and " << b << " is " << diff(a,b) << endl;
  	} else if (option == 3) {
    	cout << "The product of " << a << " and " << b << " is " << product(a,b) << endl;
  	} else if (option == 4) {
    	cout << "The division of " << a << " and " << b << " is " << div(a,b) << endl;
  	} else if (option == 5) {
    	cout << "The remainder of " << a << " and " << b << " is " << remainder(a,b) << endl;
  	}
	}

		cout << "Do you wish to make another operation? (y/n)" << endl;
  	cin >> ans;
	} while (ans == 'y');

cout << "Have a great day." << endl;
return 0;
}
