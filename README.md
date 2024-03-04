#include "ComputeUS.h"

int ComputeUS50(int CurrencyUS[], int SIZE, int Choice[0])
{
	int e;
	int i;
	int Coin50 = 50;
	
	for (i = 0; i < SIZE; i++)
	{
	 if (Coin50 > CurrencyUS[0])
	 {
		 e = 0;
		 return(e);
	 }
	e = CurrencyUS[0]/Coin50;
	CurrencyUS[0] = CurrencyUS[0] - (Coin50*e);
	}
	return(e);
    }

int ComputeUS25(int CurrencyUS[], int SIZE, int Choice[0])
{
	int f;
	int i;
	int Coin25 = 25;
	
	for (i = 0; i < SIZE; i++)
	{
	 if (Coin25 > CurrencyUS[0])
	 {
		 f = 0;
	 }
	f = CurrencyUS[0]/Coin25;
	CurrencyUS[0] = CurrencyUS[0] - (Coin25*f);
	}
	return(f);
    }

int ComputeUS10(int CurrencyUS[], int SIZE, int Choice[0])
{
	int g;
	int i;
	int Coin10 = 10;

	for (i = 0; i < SIZE; i++)
	{
	if (Coin10 > CurrencyUS[0])
	 {
		 g = 0;
		 
		} 
		 
		 g = CurrencyUS[0]/Coin10;
	CurrencyUS[0] = CurrencyUS[0] - (Coin10*g);
	}
	
	return(g);
    }


int ComputeUS1(int CurrencyUS[], int SIZE, int Choice[0])
{
	int h;
	int i;
	int Coin1 = 1;

	for (i = 0; i < SIZE; i++)
	{	
       if (Coin1 > CurrencyUS[0])
	    {
		 h = 0;
		}  
    h = CurrencyUS[0]/Coin1;
	CurrencyUS[0] = CurrencyUS[0] - (Coin1*h);
	}
	
	return(h);
    }
