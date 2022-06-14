


# Python Scope
# What is Python Scope

In programming, to access a variable or a function you should be within it's scope or space, it is a place where it is known as a variable or a function, it's a grate way to avoid name collisions.

# Using the LEGB Rule for Python Scope

The letters stand for Local, Enclosing, Global, and Built-in, which are the python scope for names, currently I will only be mentioning on the Global and somthing else called nonlocal, but first lets look at locals and globals.

Local/function scope: this is the body of any python function, where all the variables defined within it are only access by that scope.

Note: this scope is created at function call.

example on local scope:

def function_local(): x = 1 y = 3 return x + y function_local()
Global/module scope: this is the top-level scope, anything defined in this scope can be access in any other scope.

The moment a python project is started the programmer will be at the global scope so anything that is not inside a class or a function is considered in the global scope.

example:

names_list = ['x', 'y', 'z'] # this is a global variable def funcation(): # doing somthing funcation()

Global variables can be modified from any place in the python program they are included in but it's considered a bad practice to do so, as it may lead to difficulties in debugging the code, and unusable hard to understand code, and thats why it is recommended to use local names rather than global names, and to do so you need to:

Write functions that self-contained and use local names rather than global names.
Avoid modifying global name in your programs.
Avoid cross-module modifications for variable names.
Use global names as constants in your programs.
# Modifying the Behavior of a Python Scope

## The global Statement:

Using this statement allows you to define a list of names that are going to be treated as global names, but of course this is generally a bad practice and shouldn't be used as it may lead to buggy code.

## The nonlocal Statement:

These can be accessed just like global names, but the difference is that these can't be assigned nor updated, in order
  modify them you need to use 
 the "nonlocal" statement first,




## Resources

[sources1](https://realpython.com/python-scope-legb-rule/)

[sources2](https://www.youtube.com/watch?v=5Uqawfl0VHQ)

[sources3](https://artofproblemsolving.com/wiki/index.php/Basic_Programming_With_Python#Program_Example_1_3)

## Things I want to know more about

Practice more to get a better understanding of the scope concep