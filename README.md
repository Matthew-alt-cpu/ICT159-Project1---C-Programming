#include "ComputeAU.h"

int ComputeAU50(int CurrencyAU[], int SIZE, int Choice[0])
{
	int a;
	int i;
	int Coin50 = 50;
	
	for (i = 0; i < SIZE; i++)
	{
	 if (Coin50 > CurrencyAU[0])
	 {
		 a = 0;
		 return(a);
	 }
	a = CurrencyAU[0]/Coin50;
	CurrencyAU[0] = CurrencyAU[0] - (Coin50*a);
	}
	return(a);
}

int ComputeAU20(int CurrencyAU[], int SIZE, int Choice[0])
{
	int b;
	int i;
	int Coin20 = 20;
	
	for (i = 0; i < SIZE; i++)
	{
	 if (Coin20 > CurrencyAU[0])
	 {
		 b = 0;
	 }
	b = CurrencyAU[0]/Coin20;
	CurrencyAU[0] = CurrencyAU[0] - (Coin20*b);
	}
	return(b);
}

int ComputeAU10(int CurrencyAU[], int SIZE, int Choice[0])
{
	int c;
	int i;
	int Coin10 = 10;

	for (i = 0; i < SIZE; i++)
	{
	if (Coin10 > CurrencyAU[0])
	 {
		 c = 0;
		 
		} 
		 
		 c = CurrencyAU[0]/Coin10;
	CurrencyAU[0] = CurrencyAU[0] - (Coin10*c);
	}
	
	return(c);
}


int ComputeAU5(int CurrencyAU[], int SIZE, int Choice[0])
{
	int d;
	int i;
	int Coin5 = 5;

	for (i = 0; i < SIZE; i++)
	{	
       if (Coin5 > CurrencyAU[0])
	    {
		 d = 0;
		}  
    d = CurrencyAU[0]/Coin5;
	CurrencyAU[0] = CurrencyAU[0] - (Coin5*d);
	}
	
	return(d);
}
