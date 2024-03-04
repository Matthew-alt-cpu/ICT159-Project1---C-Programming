# 3.Algorithm

**Algorithm Strategy:**

Developing an Algorithm is a vital step to any program creating process along with testing through the algorithm. Developing a suitable Algorithm allows for any programmer to analyse their thought process for creating the program and how the overall program will function. I have developed a very brief Algorithm strategy as to allow my Algorithm process to cover all areas of the problem in a way that allows for a simplistic view of the program and a more detailed walkthrough that allows for a more thorough view. I will be splitting my Algorithm into a General Step-by-Step process, a more thorough Outline Process with both the equations and and a Test Sample included and I will also be splitting the Expected .c files into separate Algorithms along with a separate Main.c File Algorithm

**General Step-by-Step Algorithm:** 

This Algorithm has no equations set up or specifications and is mainly used for me to gauge how the program will be functioning in a basic fashion. I will then expand on their requirements, conditions, and functions to be used in required steps.

1)	Prompt the user for their desired currency type:
   
-	Check for valid input, Invalid Inputs prompt for new input
  
2)	Read the users chosen currency type
   
3)	Prompt the user for a valid input amount based off their chosen form of currency:
   
-	Check for valid input, Invalid inputs prompt for new input
  
4)	x <- Read Users input amount
 	
5)	Store input amount into an array
 	
6)	Factor in the different amounts available within that currency type
 	
7)	Create Variables for the amounts
 	
-	Also create variables to represents the quantity of the amounts
  
8)	Divide the total input amount with the highest currency amount within the type, then subtract the highest currency times the allocated variable from the input amount to set new input amount.
 	
-	Only Account for how many of each amount can be divided with 0 remainders
  
-	Work down with the other amounts in descending order (This is to allow for the Minimum number of coins to be given as the higher amounts are processed first)
  
9)	Process the result of the total in each different amount
 	
10)	Read the Results to the user
 	
11) Prompt user if they would like to continue or exit the program


**Thorough Outline Process Algorithm**

This Algorithm is used to further expand on the previous general one. Here is where all the test samples for the algorithm will be used to gauge the efficiency of the program. It is a lot longer and analyses what functions, equations and conditions will be used in the program. (Any changes I make throughout the entire process of the assignment will be shown)

Algorithm Example I will be using “AU” and “85 cents”
Revisions to Algorithm are Noted in Red

1)	Prompt the user “Select a number that corresponds with your desired form of Currency, 1) AU, 2) Euro, 3)US”
   
-	Check for valid input, Invalid Inputs prompt for new input
  
-	(Invalid inputs include anything not specified in the prompt)

2)	AU <- Read users chosen Currency Type

-	Set Correct Functions to Chosen Currency Type

3)	Prompt the user, “Input the desired amount to be withdrawn”
   
-	Check if input amount is valid, Invalid Inputs prompt for new input
  
-	Input must be an integer in AU and must be equal to or greater than 5, less than 96 and a multiple of 5
  
-	Input in EU must be an integer equal to or greater than 1 and less than 96
  
-	Input in US must be an integer equal to or greater than 1 and less than 96

4)	x <- “85” Read users input amount as integer
   
5)	Store input amount into an Array
   
6)	Factor Amounts in currency specified 
-	Eg: AU, 50c, 20c, 10c, 5c
-	Set Variables Coin50, Coin20, Coin10, Coin5 for Amounts
(Revised Step after Test Input 3, needed to set multiple extra variables for the program to output a Multiple of an amount)

7)	If Coin50, Coin20, Coin10, Coin5 > x, set the greater amounts to “0”
(Revised Step, set the amounts to 0 if greater than the inputted value)
-	Create Variables a, b, c, d 

8)	Divide the total input amount by the greatest amount in the currency and set the new “x” to be a subtraction by the greatest amount times the allocated variable
   
-	Work down with the other amounts in descending order (This is to allow for the Minimum number of coins to be given as the higher amounts are processed first)

-	Input Amount “x” 


		a = x/Coin50          |  a = 85/50    a = 1

		x = x – (Coin50 * a)  |  x = x –(50*1)    x = 35

(Revised, run a check if b, c, d, > 0 if true set to 0)

		b = x/Coin20          |   b = 35/20    b = 1

		x = x – (Coin20 * b)  |   x = x – (20*1)  x = 15  

-	Check if c, d, > 0 if true set to 0)
  

		c = x/Coin10          |   c = 15/10    c = 1

		x = x – (Coin10 * c)  |   x = x –(10*1)x = 5    

		d = x/Coin5           |   d = 5/5      d = 1

-	x= 0 (Possibly unnecessary but better to set the integer to a value that won’t interfere) 

9)	a, b, c, d <- Store the results of each variable
    
10)	Display, “From the input amount “85c”, the total number of 50c, you receive is “1 “, 20 cents is “1“, 10 cents is “1 “ and 5 cents is “1 “.


•	First Change to be made to the Algorithm, Equation for working out the Number of coins in the Input Amount. 

-	a = A/a (“a” being the currency amount eg: 50c)
  
-	A = A – a (“A” being the input amount being set to a new total)
  
•	Another Change that I implemented to shorten the code a bit, is by taking out the “Greater than” Check between the variables and “x” between each formula. It is unnecessary as the formula will still render the variable as “0” if it is greater than “x”

•	If a User chooses the “AU” currency type, I also added a Check to see if the integer inputted by the user is a multiple of “5” otherwise it is rendered invalid as AU currency can’t return anything below 5.

**Algorithm in Planned Program format:**

**Main. C File**

1)	Prompt the user “Select a number that corresponds with your desired form of Currency, 1) AU, 2) Euro, 3)US”
   
-	Check for valid input, Invalid Inputs prompt for new input
  
-	(Invalid inputs include anything not specified in the prompt)
  
2)	x <- Read users chosen Currency Type
 
-	Set Correct Functions to Chosen Currency Type
  
-	ComputeAU(50, 20, 10, 5)
  
-	ComputeUS(50, 25, 10, 1)
  
-	ComputeEuro(20, 10, 5, 1)
  
3)	Prompt the user, “Input the desired amount to be withdrawn”
 
-	Check if input amount is valid, Invalid Inputs prompt for new input
  
-	Input must be an integer in AU and must be equal to or greater than 5, less than 96 and a multiple of 5
  
-	Input in EU must be an integer equal to or greater than 1 and less than 96
  
-	Input in US must be an integer equal to or greater than 1 and less than 96
  
4)	Print Outputs of the Functions for each Coin Value
 	
-	The number of “#” Coins received is “#”
  
-	The number of “#” Coins received is “#”
  
-	The number of “#” Coins received is “#”
  
-	The number of “#” Coins received is “#”
  
5. Prompt user if they would like to continue or exit the program


**ComputeAU.c File **

This file will hold the 4 functions for the AU Currency Type

1)	Declare function of ComputeAU50
   
2)	Create Variables and Coin50
	
3)	Set Coin50 = 50
   
4)	For loop to run through the array once
   
5)	Check if Coin50 > x
-	If True set variable a to 0
  
6)	If False perform equation:
   
		a = x / Coin50

		x = x –(Coin50*a)

		return(a)

The ComputeAU.c File has 3 other functions within it that Function the same way as the AU50 Function, (AU20, AU10, AU5). The Function is easily reusable with only slight changes to the variables and the amounts used.


**ComputeUS.c File**

The file will hold the 4 functions for the US Currency Type

1)	Declare function of ComputeUS50
   
2)	Create Variables e and Coin50
   
3)	Set Coin50 = 50
   
4)	For loop to run through the array once
   
5)	Check if Coin50 > x
   
-	If True set variable e to 0
  
6)	If False perform equation:
   
		e = x / Coin50

		x = x –(Coin50*e)

		return(e)

All 3 of the separate files can easily run the same formula with only the slight changes to the variables and the Coin Amounts. This File also holds the 3 other ComputeUS Functions, (US25, US10, US1).

**ComputeEU.c File**

The file will hold the 4 functions for the US Currency Type

1)	Declare function of ComputeEU20
   
2)	Create Variables k and Coin20
   
3)	Set Coin20 = 20
   
4)	For loop to run through the array once
   
5)	Check if Coin20 > x
   
-	If True set variable k to 0
  
6)	If False perform equation:
 	
		k = x / Coin20

		x = x –(Coin20*k)

		return(k)

These 3 functions also have their chosen Currency-Type stored in an array and passed to them as parameter. Once again this file hold the 3 other functions of the ComputeEU Currency Type, (EU25, EU10, EU5, EU1)

**Desk Checking Test Samples:**

**Testing Sample Choices:**

With this program there is a broad range of test samples that we can use to accurately determine the efficiency and effectiveness of the program. For my Algorithm I will be using only one test table as I am not sure on the effectiveness of my method for a function that accurately tells the program which type of currency the user will be using. At the moment I have an Integer selection method that in theory works well however in a compiling program I am not totally sold on its practicality. 

The output of the program is one that is required to be specific in that there are many integers outputs that all need to be accurately represented after each execution of the program. This leads to numerous test samples that can be used to test whether the programs output is correct in this regard, for eg: If we were to display a result of only one 50 cent coin back, we also should display the fact that the program has deduced that the user receives 0 coins back of the other amounts. Each amount can be tested in this regard.

Usually, I would include a negative integer Test Sample, however since we already test for a value sub the minimum accepted input in “0”, essentially it is covered.

Test Samples used for the Algorithm: 1) 85, 2) 50, 3) 45, 4) 96, 5) 0, 6) 5, 7) 1, 8) 95, 9) 65.8 10) Null, 11) “a”. (Test Input 1 used in Original Algorithm)


Test Input 2: 50

1)	 “Select a number that corresponds with your desired form of Currency,
   
1.	AU, 2.   Euro, 3.   US”
   
2)	AU <- Read users chosen Currency Type
   
-	Check Input is Valid, if not prompt for new input
  
3)	Prompt the user, “Input the desired amount to be withdrawn”
   
4)	x <- “50” Read users input amount as integer
   
-	Check input amount is an integer that is equal to or greater than 5, less than 96 and multiple, if not prompt for new input
  
5)	Store input amount into an array
   
6)	Factor Amounts in currency specified
   
7)	If Coin50, Coin20, Coin10, Coin5 > x, set the greater amounts to “0”
    
-	Input Number = 50, False
  
-	Create Variables a , b, c, d
  
8)	Divide the total input amount by the greatest amount in the currency and set the new “x” to be a subtraction by the greatest amount times allocated variable
   
-	Input Amount “x” 

 		 a = x/Coin50             |       a = 50/50    a = 1

 		 x = x (Coin50*a)       |       x = x – (50*1)   x = 0
 	
-	Check if  Coin20, Coin10 or Coin5 > x
  
-	True set b, c, d  = 0
  
x = 0 (Possibly unnecessary but better to set the integer to a value that won’t interfere) (May instead set input amount back to original input amount for end result)

9)	a = 1, b = 0, c = 0, d = 0 <- Store the results of each variable
    
10)	Display, “From the input amount “50c”, the total number of 50c, you receive is “1 “, 20 cents is “0“, 10 cents is “0“and 5 cents is “0“.
    
11)	Prompt user if they would like to continue or exit the program

**Test Input 3: 45**

1)	 “Select a number that corresponds with your desired form of Currency, 1.AU, 2.Euro, 3.US”

2)	AU <- Read users chosen Currency Type 

-	Check input is valid if not prompt for new input

3)	Prompt the user, “Input the desired amount to be withdrawn”

4)	x <- “45” Read users input amount as integer

-	Check input amount is an integer that is equal to or greater than 5 and a multiple of 5, if not prompt for new input

5)	Store input amount into an array

6)	Factor Amounts in currency specified 

7)	If Coin50, Coin20, Coin10, Coin5 > x

-	Input Number = 45, Coin50 = True (a=0)

-	Create variables a, b, c, d

8)	Divide the total input amount by the greatest amount in the currency and set the new “x” to be a subtraction by the greatest amount

-	Input Amount “x” 

  		  a = x/Coin50      |       a = 45/50    a = 0
  		 x = x – (Coin50*a)|       x = x –(50*0)   x = 45
 	
- Check if Coin20, Coin10, Coin5 > x
  
- False
  
      		 b = x/Coin20      |       b = 45/20    b = 2
      		 x = x –(Coin20*b) |       x = x –(20*2)   x = 5
  
-	Check if Coin10, Coin5 > x
  
-	Coin10 = True, set c = 0, Coin5 = False
  
  		 d = x/Coin5       |       d = 5/5    d = 1
      		  x = x –(Coin5*d) |       x = x –(5*1)   x = 0


9)	a = 0, b = 2, c = 0, d = 1 <- Store the results of each variable

10)	Display, “From the input amount “45c”, the total number of 50c, you receive is “0 “, 20 cents is “2“, 10 cents is “0“and 5 cents is “1“.

11)	Prompt user if they would like to continue or exit the program

**Test Input 4: 96**

1)	“Select a number that corresponds with your desired form of Currency, 1.AU, 2.Euro, 3.US”

2)	EU <- Read users chosen Currency Type 

-	Check Input is valid, if not prompt for new input

3)	Prompt the user, “Input the desired amount to be withdrawn”

4)	x <- “96” Read users input amount as integer

-	Check input amount is an integer that is greater than or equal to 1 and less than 95 if not prompt for new input.

Test Input 5: 0

1)	“Select a number that corresponds with your desired form of Currency, 1.AU, 2.Euro, 3.US”

2)	US <- Read users chosen Currency Type 

-	Check Input is equal to or greater than 1and less than 96, if not prompt for new input

**Test Input 6: 5**

1)	“Select a number that corresponds with your desired form of Currency, 1.AU, 2.Euro, 3.US”

2)	AU <- Read users chosen Currency Type 

-	Check Input is valid, if not prompt for new input

3)	Prompt the user, “Input the desired amount to be withdrawn”

4)	x <- “5” Read users input amount as integer

-	Check input amount is an integer that is equal to or greater than 5, is less than 96 and a multiple of 5 if not prompt for new input

5)	Store input amount into an array

6)	Factor Amounts in currency specified 

7)	If Coin50, Coin20, Coin10, Coin5 > x, set the greater amounts to “0”

-	Input Number = 5, Coin50, Coin20, Coin10 = True

-	Create variables a, b, c, d

-	a, b, c = 0

8)	Divide the total input amount by the greatest amount in the currency and set the new “x” to be a subtraction by the greatest amount

- Input Amount “x” 

Can’t divide by “0” not sure if this will cause a problem in the program may need to change

     	 a = x/Coin50          |       a = 5/50    a = 0

 	     x = x – (Coin50*a)|       x = x –(50*0)   x = 5

         b = x/Coin20         |       b = 5/20    b = 0
           x = x –(Coin20*b)|       x = x –(20*0)   x = 5
               
        c = x/Coin10        |        c = 5/10    c = 0
           x = x –(Coin10*c)|       x = x –(10*0)   x = 5
    
         d = x/Coin5        |       d = 5/5    d = 1
            x = x –(Coin5*d)|       x = x –(5*1)   x = 0



9)	a = 0, b = 0, c = 0, d = 1 <- Store the results of each variable

10)	Display, “From the input amount “5c”, the total number of 50c, you receive is “0 “, 20 cents is “0“, 10 cents is “0“and 5 cents is “1“.

11) Prompt user if they would like to continue or exit the program

**Test Input 7: 1**

1)	“Select a number that corresponds with your desired form of Currency, 1.AU, 2.Euro, 3.US”

2)	EU <- Read users chosen Currency Type 

-	Check Input is valid, if not prompt for new input

3)	Prompt the user, “Input the desired amount to be withdrawn”

4)	x <- “1” Read users input amount as integer

-	Check input amount is an integer that is equal to or greater than 1, is less than 96 if not prompt for new input

5)	Store input amount into an array

6)	Factor Amounts in currency specified 

7)	If Coin20, Coin10, Coin5, Coin1 > x, set the greater amounts to “0”

-	Input Number = 1, Coin20, Coin10, Coin5 = True

-	Create variables a, b, c, d

-	a, b, c = 0

8)	Divide the total input amount by the greatest amount in the currency and set the new “x” to be a subtraction by the greatest amount

-	Input Amount “x” 

Can’t divide by “0” not sure if this will cause a problem in the program may need to change

 	     a = x/Coin20          |       a = 1/20    a = 0

 	     x = x – (Coin20*a)|       x = x –(20*0)   x = 1

        b = x/Coin10         |       b = 1/10    b = 0
            x = x –(Coin10*b)|       x = x –(10*0)   x = 1
               
        c = x/Coin5        |        c = 1/5    c = 0
           x = x –(Coin5*c)|       x = x –(5*0)   x = 1
    
        d = x/Coin1        |       d = 1/1    d = 1
           x = x –(Coin5*d)|       x = x –(1*1)   x = 0


9)	a = 0, b = 0, c = 0, d = 1 <- Store the results of each variable

10)	Display, “From the input amount “1c”, the total number of 20c, you receive is “0 “, 10 cents is “0“, 5 cents is “0“and 5 cents is “1“.

11) Prompt user if they would like to continue or exit the program

**Test Input 8: 95**

1)	“Select a number that corresponds with your desired form of Currency, 1.AU, 2.Euro, 3.US”

2)	US <- Read users chosen Currency Type 

-	Check Input is valid, if not prompt for new input

3)	Prompt the user, “Input the desired amount to be withdrawn”

4)	x <- “95” Read users input amount as integer

-	Check input amount is an integer that is equal to or greater than 1 and is less than 96 if not prompt for new input

5)	Store input amount into an array

6)	Factor Amounts in currency specified 

7)	If Coin50, Coin25, Coin10, Coin1 > x, set the greater amounts to “0”

-	Input Number = 1, All False

-	Create variables a, b, c, d

8)	Divide the total input amount by the greatest amount in the currency and set the new “x” to be a subtraction by the greatest amount

-	Input Amount “x” 
                        a = x/Coin50          |       a = 95/50    a = 1
          x = x – (Coin50*a)|       x = x –(50*1)   x = 1

     b = x/Coin25         |       b = 45/25    b = 1
         x = x –(Coin25*b)|       x = x –(25*1)   x = 20
               
      c = x/Coin10        |        c = 20/10    c = 2
         x = x –(Coin10*c)|       x = x –(10*2)   x = 0
    
       d = x/Coin1        |       d = 0/1    d = 0
          x = x –(Coin5*d)|       x = x –(1*0)   x = 0


9)	a = 1, b = 1, c = 2, d = 0 <- Store the results of each variable

10)	Display, “From the input amount “95c”, the total number of 50c, you receive is “1 “, 25 cents is “1“, 10 cents is “2“and 1 cents is “0“.

11)	Prompt user if they would like to continue or exit the program


**Test Input 9: 65.8**

1)	“Select a number that corresponds with your desired form of Currency, 1.AU, 2.Euro, 3.US”
   
2)	AU <- Read users chosen Currency Type
   
-	Check Input is valid, if not prompt for new input
  
3)	Prompt the user, “Input the desired amount to be withdrawn”
 	
4)	x <- “65.8” Read users input amount as integer
 	
-	Check input is an integer amount that is equal to or greater than 5, is less than 96 and divisible by 5

