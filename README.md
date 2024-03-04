# ICT159 Assignment 1:

# Student Name: Matthew 

# Operating System Used: Windows

# 1.	Assumptions

When creating any program, assumptions will always be made regarding not only how the program should be implemented but in which form of implementation will be the most efficient and redeem the most accurate results that do not possess any form of bug and that align with goal of the program.  Upon analysing the assignment in question there are many assumptions that can be drawn about the overall project.

1)	Assumptions of the multiple forms of Currency: The first main assumption to make note of will be of the user’s choice of input. The user has the option to decide on three different forms of currencies which are all noticeably different to a certain degree, this leads to a few assumptions that can be made about each form of currency and what they entail.

•	They will handle the input type as the same variable.

•	They will share a few options of output as each other.

•	They will differ in a few forms of outputs.

•	The difference in their currency amounts will impact on each other currency value within the currency groups

•	The input of the user will affect their chosen currency type (Will need to include a function to deter invalid amounts to currencies that cannot process certain value amounts)

2)	Assumptions of the Variable-type used: The most obvious and straightforward assumption to be made due to the fact there would be a decimal point in both the input and output of the program, that the type of variable we will be using will be a “float” variable, however when working with a numerical value in a program, it is much easier to instead treat the input and output as that of the variable type “integer”. In most cases it’s safe to assume that an integer type variable will be productive when performing most mathematical equations. An integer variable type can be assumed to still store the value of a post-decimal “cents” input if it is treated as a whole number throughout the process.
  
3)	Assumptions of the Scale of the program: Aside from the necessary functions that will need to be implemented in the main.c application of the program, inclusive of but not limited to; The deterring of invalid inputs, the re-prompting of the user for a valid input, the option of terminating the program, we can assume that separate libraries of functions will be established as there are many forms of output with varying results that need to be correctly processed by the program. We can assume that many of the functions established can be processed within the same designated choice of currency type. The algorithmic side of the program will also need to be extensive, moreso then seen in previous tasks.
   
4)	Assumptions of the Problem in general: There is a lot of assumptions that can be made of the problem given itself. One big factor is that the user will be making multiple inputs to the program of different scales and types. The problem comes with it the need for a set of functions to resolve the problem that also differ between 1) The Inputs declared currency type and 2) The Inputs declared currency amount; the problem also comes with it the need for applying different functions for various invalid inputs that the program will need to handle.
	
5)	Assumptions of the Programs Output: The programs output will need to be incredibly specific to each form of input. It will need to distinguish different values and types of currency and how to properly analyse the users chosen input. It can be assumed that multiple functions will need to be used to allow the program to accurately choose specific amounts based on the input given.
   
6)	Assumptions of the Modular Programming aspect: Judging from the problem presented the most optimal way to present a modular program would be to split it up into 4 separate files. Each file, other than the main file, will hold within it 1 Currency type, either “AU”, “US” or “EU” and all the appropriate formula required.
	
7)	Obscure Assumptions that may need to be tackled: These assumptions may seem more on the unnecessary side for this stage however there is value in acknowledging these assumptions as these factors could affect the way the program runs in the future, mostly in regard to decisions made by the user throughout the program. As the user being an individual who is flawed and the program that is assumed to be accurate at all times, it can be assumed that the latter should be able to account for regular user input mistakes that could happen throughout the compiling process, for eg:
   
•	Could the user make a mistake in their input and wish to re-enter the amount?

•	Could the user make a mistake with their chosen currency type?

•	Could the user make a mistake within their chosen currency type due to the amount used?

•	Could the user wish to confirm the amount being processed by the A.I. during the final steps?

•	Could the user wish to terminate the program at any given time?

Although most of these scenarios will not be handled in this program itself, I do see value in recognizing that assuming these events are possible will aid any future program creation endeavours.
