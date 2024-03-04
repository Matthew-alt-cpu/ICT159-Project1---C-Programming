#include "ComputeEU.h"

int ComputeEU20(int CurrencyEuro[], int SIZE, int Choice[0])

{

int j;

int i;

int Coin20 = 20;
	
	for (i = 0; i < SIZE; i++)
	{
	 if (Coin20 > CurrencyEuro[0])
	 {
		 j = 0;
		 return(j);
	 }
	j = CurrencyEuro[0]/Coin20;
	CurrencyEuro[0] = CurrencyEuro[0] - (Coin20*j);
	}
	return(j);
    }

int ComputeEU10(int CurrencyEuro[], int SIZE, int Choice[0])

{

int k;
 
int i;
 
int Coin10 = 10;
	
	for (i = 0; i < SIZE; i++)
	{
	 if (Coin10 > CurrencyEuro[0])
	 {
		 k = 0;
	 }
	k = CurrencyEuro[0]/Coin10;
	CurrencyEuro[0] = CurrencyEuro[0] - (Coin10*k);
	}
	return(k);
    }

int ComputeEU5(int CurrencyEuro[], int SIZE, int Choice[0])

{

int l;

int i;
 
int Coin5 = 5;

	for (i = 0; i < SIZE; i++)
	{
	if (Coin5 > CurrencyEuro[0])
	 {
		 l = 0;
		 
		} 
		 
		 l = CurrencyEuro[0]/Coin5;
	CurrencyEuro[0] = CurrencyEuro[0] - (Coin5*l);
	}
	
	return(l);
    }


int ComputeEU1(int CurrencyEuro[], int SIZE, int Choice[0])

{
int m;
 
int i;
 
int Coin1 = 1;

	for (i = 0; i < SIZE; i++)
	{	
       if (Coin1 > CurrencyEuro[0])
	    {
		 m = 0;
		}  
    m = CurrencyEuro[0]/Coin1;
	CurrencyEuro[0] = CurrencyEuro[0] - (Coin1*m);
	}
	
	return(m);
     }
