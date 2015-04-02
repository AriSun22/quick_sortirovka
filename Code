/*!
\file Sortir.cpp
\brief Заголовочный файл с описанием классов

Данный файл содержит в себе определения основных 
классов, используемых в демонстрационной программе
*/
#include "stdafx.h"
#include <ctime>
#include <locale.h>
#include <iostream>
using namespace std;


const int n=7;
int first, last; //первое число, последнее число
/**
	Функция сортировки
	*/

void quicksort(int *mas, int first, int last)
{
int mid, count; // опорное число, итоговое число
int f=first, l=last;
mid=mas[(f+l) / 2]; //вычисление опорного элемента
	do
	{
		while (mas[f]<mid) f++;
		while (mas[l]>mid) l--;
		if (f<=l) //перестановка элементов
		{
			count=mas[f];
			mas[f]=mas[l];
			mas[l]=count;
			f++;
			l--;
		}
	} 
		while (f<l);
		if (first<l) quicksort(mas, first, l);
		if (f<last) quicksort(mas, f, last);
}

//!Главная функция
void main()
{

setlocale(LC_ALL,"Rus");

int *A=new int[n];

 for(int i=0;i<n;i++)
    {
        cout<<endl; //Ввод массива
        cin>>A[i];
    }
first=0; last=n-1;

quicksort(A, first, last); // вызов функции
cout<<endl; //результат

	for (int i=0; i<n; i++) cout<<A[i]<<" ";
	delete []A;

system("pause>>void");
}
