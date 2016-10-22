// DataStructuresExercise.cpp : 定義主控台應用程式的進入點。
//

#include "stdafx.h"
using namespace std;

int main()
{
	int n = 200;
	int arr[MAX_SIZE];
	srand(time(NULL));
	for (int i = 0; i < n;i++) {
		arr[i] = rand() % 1000;
	}
	cout << "Before SelectionSort, Array : " << endl;;
	for (int i = 0; i < n;i++) {
		cout << arr[i] << " ";
	}
	cout << endl;
	selectionSort(arr, n);
	cout << "After SelectionSort, Array : " << endl;
	for (int i = 0; i < n; i++) {
		cout << arr[i] << " ";
	}
	cout << endl;
	system("pause");
	return 0;
}

void selectionSort(int x[], int n) {
	int i, j, min, temp;
	for (i = 0; i < n - 1;i++) {
		min = i;
		for (j = i + 1; j < n;	j++) {
			if (x[j]< x[min]) {
				min = j;
			}
			SWAP(x[i], x[min], temp);
		}
	}
}
