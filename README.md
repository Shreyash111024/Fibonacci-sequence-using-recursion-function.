# Fibonacci-sequence-using-recursion-function.



Research ~ 
 ⧫ What is a Recursive Function?
In C programming, a recursive function is a function that calls itself, either directly or indirectly, during its execution. This technique is used to solve problems by breaking them down into smaller, similar subproblems until a base case is reached.

Base Case: This is the crucial termination condition that stops the recursion. Without a properly defined base case, a recursive function would call itself indefinitely, leading to a stack overflow. The base case defines the simplest form of the problem that can be solved directly without further recursion.
Recursive Step: This is the part of the function where it calls itself, but with modified arguments. The modification of arguments is essential to ensure that each subsequent recursive call moves closer to the base case, eventually leading to termination. The recursive step typically breaks down the problem into smaller, similar subproblems.
Self-Reference: A recursive function inherently involves self-reference, meaning the function's definition includes a call to itself. This is the defining characteristic of recursion.
Elegance and Readability (for certain problems): For problems with an inherently recursive structure, a recursive solution can often be more concise and easier to understand than an iterative approach using loops. However, for other problems, an iterative solution might be more efficient or clearer.



Analysis ~    
Structure of a Recursive Function:

A recursive function in C consists of two main parts:
Base Case: This is the condition that terminates the recursion, preventing infinite loops. When the base case is met, the function returns a value without making further recursive calls.
Recursive Case: This part makes a recursive call to the same function with modified arguments, moving closer to the base case.

Advantages of Recursion:
Code Simplicity and Readability: For problems with inherent recursive structures (e.g., tree traversals, factorial calculation), recursion can lead to more concise and elegant code compared to iterative solutions.
Natural Fit for Divide-and-Conquer: Recursion is well-suited for algorithms that follow a divide-and-conquer strategy, such as quicksort, merge sort, and binary search.
Handling Recursive Data Structures: It simplifies the manipulation of recursive data structures like trees and graphs.

Disadvantages of Recursion:
Overhead of Function Calls: Each recursive call adds a new stack frame to the call stack, consuming memory and potentially leading to stack overflow errors for deep recursions.
Performance: Recursive solutions can sometimes be slower than iterative solutions due to the overhead of function calls.
Debugging Complexity: Debugging recursive functions can be more challenging due to the multiple function calls and the call stack's behavior.
Applications of Recursion
Recursion is widely used to solve different kinds of problems from simple ones like printing linked lists to being extensively used in AI. Some of the common uses of recursion are:
Tree-Graph Algorithms
Mathematical Problems
Divide and Conquer
Dynamic Programming
In Postfix to Infix Conversion
Searching and Sorting Algorithms



Related code and more information.

Ideate~    
The Fibonacci sequence is a series of numbers where each number is the sum of the two preceding ones, usually starting with O and 1. A recursive approach to finding a Fibonacci number involves a function that calls itself. It defines a base case (for n = 0 and n = 1 f the function returns 0 and 1 respectively) and a recursive step where the function returns the sum of the function called with n 1 and n 2

How it works
Base Case: The recursion stops when it reaches the first two numbers of the sequence, which are 0 and 1.
Recursive Step: For any number greater than 1, the function calls itself to find the sum of the two previous numbers in the sequence. For example, the function for the 5th number (F5) would call itself for the 4th (F4) and 3rd (F3) numbers, and so on, until it reaches the base cases of F₁ and Fo.

Recursive formula
The Fibonacci sequence can be defined by the following recursive formula:
FnFn-1+Fn-2 for n >= 2
F_{0} = 0
F_{1} = 1

   For more information click here.

Build ~ 
#include <stdio.h>


int fib(int n) {
   
    if (n == 0) {
        return 0;
    } else if (n == 1) {
        return 1;
    }
    
    else {
        return (fib(n - 1) + fib(n - 2));
    }
}

int main() {
    int n, i;

    printf("Enter number of terms: ");
    scanf("%d", &n);

    printf("Fibonacci Series: ");

    
    for (i = 0; i < n; i++) {
        printf("%d ", fib(i));
    }
    printf("\n");

    return 0;
}

Test Cases ~ 
Test Case 1-
Enter number of terms: 5
Fibonacci Series: 0 1 1 2 3 
Test Case 2-
Enter number of terms: 10
Fibonacci Series: 0 1 1 2 3 5 8 13 21 34 

Implementation~
https://github.com/Shreyash111024/Fibonacci-sequence-using-recursion-function..git

