# Largest-number-array
#displays the largest number from 10 values 
#include<iostream>
#include<array>
#include<algorithm>
#include<random>
using namespace std;
int main()
{
	int max, array[10];
	cout << "Enter 10 integer values: " << endl;
	for (int j = 0; j < 10; j++)
	{
		cout << "Number " << j + 1 << " : ";
		cin >> array[j];
		while (cin.fail() || array[j] < 0 || array[j] > 100)
		{
			cout << "\n\aThe number entered is not within the range of 1-100! "<<endl;
			cout << "Enter the number again : ";
			cin.clear();
			cin.ignore();
			cin >> array[j];
		}
	}
	for (int j = 0; j < 10; j++)
	{
		if (array[0] < array[j])
			array[0] = array[j];
	}
	cout << "\nThe largest number is: "<<array[0];
	return 0;
}
