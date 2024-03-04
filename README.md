# 7. Self Assessment

Throughout my process of designing my Algorithm and Program, I plan to constantly update this section with information in regards to both my overall performance and the overall performance of my Algorithm / Program.

**A Self-Assessment of my Assumptions in comparison to the result of the program:**

I had a lot of assumptions of both the problem and the program I would be developing, at the beginning of my analysis of the problem. My initial concern was with all the different types of invalid inputs that could appear within the compiling process. The user has the option of choosing their form of currency to start with then a follow up of the input amount they desired. I had a few ideas on how I would tackle the choice aspect of the user picking their form of currency, but my initial concern was moreso in regard to how to ensure my program only compiles the functions that are associated with the specified type of currency. 

At the end of the program, I found that majority of the invalid inputs that I needed to deal with have been dealt with. Unfortunately, the only invalid input I was unable to counter was the input of a floating-point number in the integer input, after a lot of testing I was unable to come up with a code that could counter that invalid input. The result of this a successful handle within my Algorithm of the floating-point numbers but a failure on the side of the program. My Assumption of the variable type being integer may have been the reasoning for the fault, perhaps if I had instead used a floating-point input to be converted to an integer than handling the issue would have been a lot simpler.

The Assumptions I had for the scale of the program were relatively accurate. I assumed the Algorithm would be extensive in that not only would there be separate libraries of functions that that needed Algorithmic planning, but a lot of functions needed to be add3ed to the main program in order to deter invalid inputs of two separate queries to the input user. This is a slight contrast to what I was used to in that generally the tasks we have been performing throughout the semester have involved the single input from the user.

From my assumptions of the modular aspect of the program, I was correct in that 4 separate c files would need to be created and although I did not specify the header files included they were most definitely in my thought process, in future however I will need to make sure I also list that or make a mention of them in my Assumptions.

In terms of the obscure Assumptions I noticed for myself one form of input that I had wanted to implement but felt was unnecessary for the project was including a function in which at any given time, specified early by the program, the user could cancel the ongoing process as if to simulate the idea of an individual making a mistake through their chosen currency type of the input amount they desired. This would have also been followed up with a prompt check before processing the output to confirm the final input amount which would have helps simulate a real-life scenario.

**As I finish my Algorithm:**

Surprisingly the Algorithm went a lot smoother than expected. Originally, I assumed that I would need a lot of complex formulas and equations to get to my desired result, however after some thought the end formulas (assuming they function correctly), should give me the results I expect. At this point in time however I still feel the main challenge will be the allocation of the formulas based off the individuals desired currency type and ensuring the other formulas for the types not included to not impede on the overall process. There was still an extensive amount in my Algorithm Planning, a lot of which I think became very useful for the overall process. My Algorithm in which I took an example from my Sample Inputs, helped me gauge a visual check on the problems that could occur throughout the process, I had decided to implement this simulated desk check with corrections to also help me record the changes that needed to be made to my functions and equations.

**After Desk Checking My Algorithm:**

Included in my Algorithm section I have also included all my desk checking of the Sample Inputs for my Table charts. This step was the most crucial in the overall success of the program and process as a few necessary change to the algorithm were discovered here that if were not discovered would have led to a failed program. The initial and possibly most crucial fix for the algorithm was of the equation after discovering its ineffectiveness for handling the output of multiples of the same coin going into the input number. It was through the desk checking that I could see that my 20c were not returning in multiples and the input figure would not change appropriately for the next equation. It was than where I made the appropriate change to add a new group of basic variables that could simulate the frequency a coin could be divided into the input number.

Another feature of the Algorithm I noticed that was unnecessary and led to a less aesthetic and pleasant program was the check of coins being greater than the  input amount. Initially I had every coin checked multiple times to see if it was greater then  the input amount as to allow for a constant returning of 0 if it was true, this was unnecessary, and the functions would be split within the file so only each would need to be checked once.

Another realisation from doing my desk checking was also that I had forgot to include my check for the input amount on the currency type “AU” to ensure it was a multiple of 5. In my lowest accepted input check, I realised that technically the Algorithm would accept 6, 7, 8, 9 and so on that were not divisible by 5. This was important to realise but simple to fix.  My Final main Concern I had for my program through my Algorithm was the system’s ability to handle the division of 0 in my equations. For this I ran some simple tests of equations just to make sure that the formula would work in my desired way, which thankfully it did.

**After my Algorithm Table and Program Table Checks:**

The desk checking for my Algorithm was done thoroughly and allowed for my Table Chart to display mostly successful results for the end of my algorithm. The check for the decimal point although worked in theory and this was the stark contrast between my Algorithm and Program outputs. The Program was unable to handle the float inputs which results in a failed process. In future I will need to consider moreso the value of using floating point inputs as opposed to integer inputs which I believe I relied too heavily on. I did believe the process of converting an input float that was required to be an integer would be on the same level of difficulty as the counter option however I have learned it was a lot harder for this process. My biggest take from this was to enforce the planning aspect of every function again heavily in conjunction with my chosen variable types, as there are numerous different processes that need to be considered and one gear out of place may cause the whole system to rupture.

**After finishing my Program:**

There were a few minor changes and 1 moreso major change that needed to be made between the Algorithm and the Program. The major change was in the layout of the function for the equations to determine the returning number of coins that optimally made up the input amount. My Program initially Used the previous coin equation from the previous function to attempt to adjust the input amount for the next Function. Essentially the Algorithm that I created did not specify the storing of the input amount into an array and passing it through to the function, this has taught me a vital lesson hat in my Algorithms I must also detail the fact that the users input will be stored in an array.  After coming to this conclusion and initializing it in my program, the program and functions all worked independently and optimally to provide the desired results.

Whilst creating my program in my initial thoughts my prompt function for the user to decide if they would terminate or restart the program was going to work based off an Integer Input due to the fact that character entries were not necessary for the Assignment however due to my eagerness to try and simulate a design that focused on a realism aspect I also made the effort to learn how to store the users character input using the strcmp( ) function from “string.h” and base a while function around the user input being “y” for yes.

After finishing my program the only flaw that I realistically would change the next time I had to create a program like this would be to accept the users input amount as a float input rather then an integer and convert it to an Integer from there. The mishandling of decimal points in the program is the only aspect I think I would change.


  **What Works:**

•	My input validity check for the Currency Type the user specifies

•	My input verification check for the Integer that the user input for the currency amount

•	Each separate C file works effectively in regards to the desired outputs

•	Using Arrays as parameters to my functions were the key to allowing my functions to return the desired outputs

•	The passing of a specific currency type to the appropriate functions also works effectively

•	My Do While Loop for the restart and continuation of the program alongside the opposite if function that allowed for the exit from the program along with the printf string attached

•	The aesthetic little inputs I inserted into my program as to allow a more pleasing performance of the program to the user’s eye. This was done through efforts such as:

-	Extra spacing

-	Attention to grammar in detail

-	Insertion of common courtesies

-	Frequency of new lines from majority of sentences

 	  ** What Does not Work:**

•	Although There aren’t many things that did not work with the program, there were some things I would have liked to have included that although were not necessary, would have been critical for simulating a realistic Bank Teller AI.

•	The handling of decimal point input amounts (Which I have now learned the value of starting with accepting float inputs)

I would have also liked to include a function to at any point prompt the user if they wish to cancel through the user’s input

•	Processing character inputs unless requested (Although not needed in the program)

**Final Summary of my Own Performance and the Assignment Overall.**

The 7th week of Tutorial work was honestly a struggle for myself which effected the first week of my assignment preparation. I struggled not so much with arrays but the passing of the arrays to functions, this is a stark contrast to the previous week where passing parameters such as regular variables I attuned to relatively simply. The struggle from this however did lead me to learn a lot about not only how to pass the arrays but the overall benefit of doing so which is heavily shown through my program.

Heading into the assignment I feel my main strengths that I have seen from myself in regards to the basic levels of programming I’ve learned so far came in the form of my initial planning eg: Creating Algorithms, Test Sampling and Test Table checks, however the assignment has taught me even further how to optimally plan for my program to be created. Aspects such as the input type being of crucial value to relative functions, and how even smaller details can overall affect other functions of the program, so they all have to be thought of as a working model to a degree rather than their own individual impact on the overall program. Will a certain input allow the function to perform accurately? This was a big consideration that although I thought was important, I did not consider its overall impact on functions like prompts for that input type.

I feel through this assignment I was able to grab a good grasp of arrays as they were vital for the overall functionality of my program. My prompts to check the users’ inputs at various times overall I feel I did a good job with, there may be possibly more optimal ways to explore handling these functions however so that is a thought process that I will also be taking away from this experience.

The Aesthetically pleasing element of the program that I find that I have implemented also gave myself insight into the designing of a program that I had not really considered before. Not only does the programs development in and of itself need to be readable and not a bunched-up mess, but the programs output should also apply a lot of the same principles when thinking of setting out the program’s development. Subtle includes of “…” or “\n\n\n” Allow for the program to spread out and not have the user focused on a whole bunch of clumped up text, the ability to spread everything out allows for the user to easily understand what the program wants them to do and what it intends to display to them.

I enjoyed creating this Algorithm and all its functions and equations along with the Program and the Assignment in general. The last 2 months of programming introduction has been an enjoyable learning experience that of which I hope is shown in my Assignment and the program I created, I take away from this assignment a lot more knowledge and understanding of different aspects of programming from the algorithm planning to the program creation itself and all its required functions.

My main take aways include:

•	Accurately detailing how the user’s input will be handled within the Algorithm

•	Paying a lot of mind to the type of input that should be created from the user

•	Extra thinking as to how certain functions that although may not seem relevant to each other could crossover within the program

•	Realism and how the AI could simulate a real-life scenario which include handling real life user mistakes

•	The Aesthetic side of the program’s development and design for both the user and the programmer

•	Being more mindful to which Variable types I will need

•	The use of Arrays and their overall benefit to the functionality of the program

•	How prompts could possibly be executed in a more efficient way as I feel this could be a possibility(not that I’m not satisfied with how they were implemented but optimality should always be a priority)

•	How to manage my own time and the effort required to create a program that performs optimally for the user.


