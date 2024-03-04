# Main.c Code

#include <stdio.h>
#include <string.h> /*included for input of character acceptance with strcmp() Function allowing for a y or n input to be processed as needed*/
#include "ComputeAU.h"
#include "ComputeUS.h"
#include "ComputeEU.h"


int main()
{

	const int SIZE = 1;    //Setting a constant amount of 1 Element for SIZE
 
    int CurrencyAU[SIZE];  //Storing Currency Amount for AU Functions
    
	int CurrencyUS[SIZE];  //Storing Currency Amount for US Functions
 
	int CurrencyEuro[SIZE];//Storing Currency Amount for EU Functions
 
	int Choice[SIZE];      //Storing the Currency-Type
 
	char Continue[1];      //Storing the char input of the user
	
	Choice[0] = 1;/* Setting the Choice Array to start at 1, allows for checks to run 
	                when appropriate otherwise impedes on perfromance*/
					
	/*Multiple "\n\n\n" added as to make the program display more spread out and not too conjested,
	  creating a more aesthetic appeal*/
	  
do //Allows for Restarting of Program if user decides

{  
                                                        
    printf("\n                     Welcome, I am the ICT159Assignment1TellerBot, i'll be assisting you today.\n\n");
    
	printf("Let's start with selecting your Currency Type.\n\nType the corresponding number for your desired Currency.\n1 for AU (Australian Currency)\n2 for US (United States of America Currency)\n3 for Euro (European Currency)\nSelection:");
 
    scanf("%d", &Choice[0]); //Storing the users Desired Currency Type
	                          
 while (Choice[0] < 1 || Choice[0] > 3) 
 
	{
 
	printf("Invalid input, please enter a valid input.\nWhich Currency Type would you like? 1 for AU, 2 for US or 3 for Euro? "); 
	scanf("%d", &Choice[0]);
 
	}

if (Choice[0] == 1 && Choice[0] != 2 && Choice[0] != 3) //Initiating the Currency Type AU Functions

{

    printf("\n.\n..\n...\nHow much AU Currency would you like?\nNOTE: AU Currency must be 5 or above, 95 or below and be divisible by 5.\nInput Amount:");
    
	scanf("%d", &CurrencyAU[0]);

while (CurrencyAU[0] > 95 || CurrencyAU[0] < 5 || CurrencyAU[0] % 5) //Checks that input is Valid for the AU Currency Type

	{
		printf("Unacceptable Amount.\nNOTE: AU Currency must be 5 or above, 95 or below and be divisible by 5.\nPlease re-enter your desired amount: ");
		scanf("%d", &CurrencyAU[0]);
	}
	int a = ComputeAU50(CurrencyAU, SIZE, Choice); // Declarations of AU Functions and returning Variables
	int b = ComputeAU20(CurrencyAU, SIZE, Choice);
	int c = ComputeAU10(CurrencyAU, SIZE, Choice);
	int d = ComputeAU5(CurrencyAU, SIZE, Choice);  
	
	printf("\n.\n..\n...\nThe number of 50cents received is %d\n", a); //Printing Returned Results
	printf("The number of 20cents received is %d\n", b);
	printf("The number of 10cents received is %d\n", c);
	printf("The number of 5cents received is %d\n", d);
}

 if (Choice[0] == 2 && Choice[0] != 1 && Choice[0] != 3) //Initiating the Currency Type US Functions
	{
	printf("\n.\n..\n...\nHow much US Currency would you like?\nNOTE: US Currency must be 1 or above and 95 or below.\nInput Amount: ");
	scanf("%d", &CurrencyUS[0]);
	
	while (CurrencyUS[0] > 95 || CurrencyUS[0] < 1) //Checks that input is Valid for the US Currency Type
	{
		printf("Unacceptable Amount.\nNOTE: US Currency must be 1 or above or 95 or below.\nPlease re-enter your desired amount: ");
		scanf("%d", &CurrencyUS[0]);
	}
	int e = ComputeUS50(CurrencyUS, SIZE, Choice); // Declarations of US Functions and returning Variables
    int f = ComputeUS25(CurrencyUS, SIZE, Choice);
    int g = ComputeUS10(CurrencyUS, SIZE, Choice);
    int h = ComputeUS1(CurrencyUS, SIZE, Choice);		
  
	printf("\n.\n..\n...\nThe number of 50cents received is %d\n", e); //Printing Returned Results
	printf("The number of 25cents received is %d\n", f);
	printf("The number of 10cents received is %d\n", g);
	printf("The number of 1cents received is %d\n", h);
	}
	
if (Choice[0] == 3 && Choice[0] != 1 && Choice[0] != 2) //Initiating the Currency Type EU Functions
	{
		printf("\n.\n..\n...\nHow much Euro Currency would you like?\nNOTE: Euro Currency must be 1 or above and 95 or below.\nInput Amount: ");
	    scanf("%d", &CurrencyEuro[0]);
	
	while (CurrencyEuro[0] > 95 || CurrencyEuro[0] < 1)//Checks that input is Valid for the EU Currency Type
	{
		printf("Unacceptable Amount.\nNOTE: Euro Currency must be 1 or above or 95 or below.\nPlease re-enter your desired amount: ");
		scanf("%d", &CurrencyEuro[0]);
	}
	int j = ComputeEU20(CurrencyEuro, SIZE, Choice); // Declarations of EU Functions and returning Variables
    int k = ComputeEU10(CurrencyEuro, SIZE, Choice);
    int l = ComputeEU5(CurrencyEuro, SIZE, Choice);
    int m = ComputeEU1(CurrencyEuro, SIZE, Choice);
	
	printf("\n.\n..\n...\nThe number of 20cents received is %d\n", j); //Printing Returned Results
	printf("The number of 10cents received is %d\n", k);
	printf("The number of 5cents received is %d\n", l);
	printf("The number of 1cents received is %d\n", m);
	}
	
	//Prompt to check if user wants to restart the program or exit the program
	printf("\n.\n..\n...\nWould you like to Continue and enter another Amount? Press 'y' to Continue\nOr would you like to exit the program? Press 'n' to Exit the Program ");
	scanf("%s", &Continue[0]); 
}

	while (strcmp(Continue, "y") == 0); //Restart program if the two strings are equal
	
	if (strcmp(Continue, "n") == 0 ) //Exit program if the two strings are equal
	{
    printf("\n.\n..\n...\nTerminating the Program, have a great day.\n\n                     Thankyou for using ICT159Assignment1TellerBot!\n\n");
	}
	
	return(0);

}

/*Overall very happy with the program and how it turned out, everything functions well with no bugs that I could find.
Unfortunately I struggled to implemement a check for Decimal point inputs on required Integer inputs. That I'd say is
the one flaw of the program as I'd also seeked a method toround the float input into an integer to no aveil.*/
