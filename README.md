# Project Overview and Task

_You should read this question as if the change giver is an artificial intelligence-based bank teller who has to give amounts of money to customers by automatically working out the amounts._

**You are asked to write a modular solution (algorithm and C program) that will accept as input an amount of money in a certain currency and return the optimal number of coins in that currency.**

The amount of money should be an integer value in the range of 1 to 95 cents inclusive. 

The program should first ask the user to select a currency among one of the following three:
1) US$, which has four types of coins of 50, 25, 10 and 1 cents 
2) AU$, which has four types of coins of 50, 20, 10 and 5 cents
3) Euro, which has four types of coins of 20, 10, 5 and 1 cents

(Note: these coins are randomly chosen just for the purpose of this exercise.)

It should then ask the user to input an amount of money (a number between 1 to 95 cents inclusive). Your program should then return the minimum number of coins (in the selected currency) that sum up into that number.

Your solution should also ensure that, if the chosen currency is the AU$, the input value should be in multiples of 5. 

Based on valid input, your solution should calculate how many coins of each denomination should be returned, and display this to the user. 

The solution should aim to give as much of the higher valued coins as possible. For example, a poor solution for an input of 30 cents would give six 5 cent coins. A correct solution would give a 20 cent coin and a 10 cent coin. 

After each output, the user should be asked whether they wish to continue (i.e., enter another amount) or exit/terminate the program. 

Your solution (algorithm and program) should be designed using a modular approach. This requires the submission of a structure chart, a high-level algorithm, and subsequent decompositions of each step (i.e. low-level algorithms).

Note that structure chart is different from flowchart. Structure chart is about the modular decomposition of the problem; please refer to the lecture slides of Week 6 (Modular Programming).

Note that for this problem, the principles of code reuse and high cohesion are particularly important and a significant number of marks are allocated to these aspects of your design.

•	You should attempt to design your solution such that it consists of a relatively small number of modules, but still meets the modular design best practice requirements of this unit. In particular, strive to have one module that can be reused (called repeatedly) to solve the coin calculation problem. If you find that you have developed a large number of modules where each performs a similar task, or that you have a lot of instructions that are repeated in one module, then attempt to analyse your design to generalise the logic so that you have just one general version of the module.

•	Be mindful of the cohesion exhibited by each module. If you have a module that is doing more than one task (i.e. demonstrating low cohesion), then you should re-design it to have high cohesion.
