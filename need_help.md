 //Need_some_help
//I'm new in coding, thus I need some help!How I can fix it?
#include <iostream>
#include<cstdlib>
#include<ctime>
using namespace std;
int main()
{
	srand(static_cast<unsigned int>(time(0))); // Запуск гениратора случайных чисел
	int seceret_number = rand() % 150+ 1; // Выставляем диапазон (+1 потому что числовой ряд начинается с 0)
	int tries = 0;
	int guess;
	cout << "\t Welcome to Number Guesser!\n\n";

do{
	cout << "Enter a guess: ";
	cin >> guess;
	++tries;
	if (guess > seceret_number)
	{
		cout << "Your number is too big!\n\n";
	}
	else if (guess < seceret_number)
	{
		cout << "Your number is too small!\n\n";
	}
	else
	{
		cout << "Yes, it is! You got it in " + tries + " tries.\n";
	}
  } while (guess != seceret_number);
return 0;
}
