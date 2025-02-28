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


# TASK2 DETAIL:-
This program uses the math module in Python to perform basic mathematical operations on a user-input number. Specifically, it calculates the square root, natural logarithm, and sine of the given number. Here's a detailed explanation of the program:

Program Walkthrough:
Importing the math module:



import math
The math module is imported at the start of the program. This module provides access to many mathematical functions like sqrt(), log(), and sin(), which are used later in the program.
Input from the user:


number = float(input("Enter a number: "))
The program prompts the user to input a number using the input() function.
The input is then converted into a floating-point number using float(). This allows the program to work with both integers and decimals.
The entered number is stored in the variable number.
Calculating the square root:

square_root = math.sqrt(number)
The function math.sqrt(number) is used to calculate the square root of the number.
The result is stored in the variable square_root.
If the user enters a negative number, this will raise a ValueError because the square root of negative numbers is undefined for real numbers (in Python, this would result in an error unless using complex numbers with cmath).
Calculating the natural logarithm:


natural_log = math.log(number)
The function math.log(number) computes the natural logarithm of the number (logarithm with base e).
The result is stored in the variable natural_log.
If the user enters a non-positive number (zero or negative), this will raise a ValueError because the natural logarithm is undefined for non-positive numbers.
Calculating the sine of the number:
sine_value = math.sin(number)
The function math.sin(number) calculates the sine of the number. Note that the argument for math.sin() is expected to be in radians.
The result is stored in the variable sine_value.
The sine of any number can be calculated, whether it's positive, negative, or zero.
Printing the results:


print(f"Square root  : {square_root}")
print(f"logarithm : {natural_log}")
print(f"Sine : {sine_value}")
The program prints the calculated results to the console using formatted strings (f-strings).
Each of the three values — square root, natural logarithm, and sine — is printed with an appropriate label.
Example Execution:
Case 1: User Input = 9
Enter a number: 9
Square root  : 3.0
logarithm : 2.1972245773362196
Sine : 0.1411200080598672
Square Root of 9: The square root of 9 is 3.0.
Natural Logarithm of 9: The natural logarithm of 9 is approximately 2.1972.
Sine of 9 (radians): The sine of 9 (where 9 is interpreted as 9 radians) is approximately 0.1411.
Case 2: User Input = 16
Enter a number: 16
Square root  : 4.0
logarithm : 2.772588722239781
Sine : -0.2879033166650653
Square Root of 16: The square root of 16 is 4.0.
Natural Logarithm of 16: The natural logarithm of 16 is approximately 2.7726.
Sine of 16 (radians): The sine of 16 (radians) is approximately -0.2879.
Key Concepts:
Square Root (math.sqrt):

The sqrt() function calculates the square root of a number, which is a value that, when multiplied by itself, gives the original number.
The result will always be a positive number, or 0 if the input is 0. For negative inputs, the function will raise an error in real numbers.
Natural Logarithm (math.log):

The log() function computes the natural logarithm (logarithm with base e) of a number.
The natural logarithm of 1 is 0, and the natural logarithm of numbers greater than 1 is positive. The logarithm is undefined for zero or negative numbers.
Sine (math.sin):

The sin() function computes the sine of a given number in radians.
The sine of 0 is 0, and the sine of positive and negative numbers will vary within the range of -1 to 1.


