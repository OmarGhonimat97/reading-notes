## Python Scope & the LEGB Rule:

The letters in the acronym LEGB stand for Local, Enclosing, Global, and Built-in scopes.

> Understanding Scope

In programming, the scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on. 

1. Global scope: The names that you define in this scope are available to all your code.
2. Local scope: The names that you define in this scope are only available or visible to the code within the scope.

> Modifying the Behavior of a Python Scope

- global names can be accessed or referenced from any place in your code.
- local names can be accessed only from inside the local Python scope they were created in or from inside a nested function.
- nonlocal names can be accessed from inside nested functions, but they can’t be modified or updated from there.

***global*** and ***nonlocal*** keywords allow you to modify the content of global and nonlocal names.

>> The global Statement

When you try to assign a value to a global name inside a function, you create a new local name in the function scope. 
o modify this behavior, you can use a global statement. With this statement, you can define a list of names that are going to be treated as global names.

The statement consists of the global keyword followed by one or more names separated by commas. You can also use multiple global statements with a name (or a list of names). 
All the names that you list in a global statement will be mapped to the global or module scope in which you define them.

>> The nonlocal Statement

nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope.

Unlike global, you can’t use nonlocal outside of a nested or enclosed function. To be more precise, you can’t use a nonlocal statement in either the global scope or in a local scope.


## BIG O notation 

- Space Complexity >> how much memory
- Time Complexity >> measure of how long an algorithm takes to do something



It's a way for comparing algorithms with each other and finding the most efficient one.

Also measuring how the algorithm will deal with very large data.

It indicates the worst case scenario for time and space complexity.

- O(1) >> Constant running time
- O(logn) >> Logarithmic running time
- O(n) >> Linear running time
- O(n logn) >> Log- Linear running time
- O(n^k) >> Polynomial running time

