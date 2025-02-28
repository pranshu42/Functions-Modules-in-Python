# Functions-Modules-in-Python
# TASK1 DETAILS:-

This program calculates the factorial of a given number using recursion. Here's a detailed breakdown of the program:

Program Walkthrough:
Input from the user:

number = int(input("Enter a number "))
The program prompts the user to enter a number.
The input() function reads the user's input as a string. We use int() to convert the string to an integer, which is stored in the variable number.
Defining the factorial function:

def factorial(n):
A function named factorial is defined that takes one parameter, n, which will be the number whose factorial we want to calculate.
Base Case:

if n == 0 or n == 1:
    return 1
In a factorial, by definition, the factorial of 0 and 1 is always 1. This is the base case of the recursion.
If the input number n is either 0 or 1, the function returns 1 directly, ending the recursion.
Recursive Case:

else:
    return n * factorial(n - 1)
If n is greater than 1, the function calls itself with the value n - 1. This is the recursive step.
The function multiplies n by the factorial of n - 1 until the base case is reached.
Calculating the Factorial and Printing the Result:

result = factorial(number)
print(f"The factorial of {number} is: {result}")
After the factorial function is defined, the program calls factorial(number) to calculate the factorial of the entered number and stores the result in the variable result.
Finally, it prints the result using print(). The f-string is used to format the output, inserting the value of number and result into the string.
Example Run:
Let’s consider an example where the user enters 5 as input.

The user enters 5.
The factorial function is called with n = 5.
Since 5 > 1, the function recursively calls itself with n = 4.
This process continues, with the function calling itself with n = 3, n = 2, and finally n = 1.
When n = 1, the base case is met, and the function returns 1.
The recursion then "unwinds," multiplying the values together: 1 * 2 * 3 * 4 * 5 = 120.
The result, 120, is printed.
Example Execution:


Enter a number 5
The factorial of 5 is: 120
How Recursion Works Here:
The recursion works by breaking the problem down into smaller subproblems:
factorial(5) = 5 * factorial(4)
factorial(4) = 4 * factorial(3)
factorial(3) = 3 * factorial(2)
factorial(2) = 2 * factorial(1)
factorial(1) returns 1 (base case)
Then, the function computes the final result by multiplying all the results together as it returns from the recursive calls.
Key Concepts:
Recursion: A function that calls itself to solve smaller instances of the problem.
Base case: The condition that stops the recursion (here, when n is 0 or 1).
Recursive case: The part of the function that calls itself to break the problem down further (here, n * factorial(n - 1)).
This program efficiently calculates the factorial of a given number using recursion. However, for very large numbers, recursion may hit the recursion depth limit (depending on the Python environment). For such cases, an iterative approach or using a built-in library function like math.factorial() could be more suitable.
