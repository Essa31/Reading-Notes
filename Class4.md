# Python Objects and Classes

Python is an object-oriented programming language. Unlike procedure-oriented programming, where the main emphasis is on functions, object-oriented programming stresses on objects.

An object is simply a collection of data (variables) and methods (functions) that act on those data. Similarly, a class is a blueprint for that object.

We can think of a class as a sketch (prototype) of a house. It contains all the details about the floors, doors, windows, etc. Based on these descriptions we build the house. House is the object.

As many houses can be made from a house's blueprint, we can create many objects from a class. An object is also called an instance of a class and the process of creating this object is called instantiation.

# Creating an Object in Python
We saw that the class object could be used to access different attributes.

It can also be used to create new object instances (instantiation) of that class. The procedure to create an object is similar to a function call.

>>> harry = Person()
This will create a new object instance named harry. We can access the attributes of objects using the object name prefix.

Attributes may be data or method. Methods of an object are corresponding functions of that class.

This means to say, since Person.greet is a function object (attribute of class), Person.greet will be a method object.

class Person:
    "This is a person class"
    age = 10

    def greet(self):
        print('Hello')


 create a new object of Person class
harry = Person()

 Output: <function Person.greet>
print(Person.greet)

Output: <bound method Person.greet of <__main__.Person object>>
print(harry.greet)

 //Calling object's greet() method

 //Output: Hello
harry.greet()
Run Code
Output



<function Person.greet at 0x7fd288e4e160>
<bound method Person.greet of <__main__.Person object at 0x7fd288e9fa30>>
Hello

[sourse](https://www.programiz.com/python-programming/class)

# Think Recursively in python

## Train Your Mind to Think Recursively in 5 Steps

How to solve recursive problems easily?

# 1- Use the iterable-approach first.
This step is relatively simple for most people. We have a number and want to sum its digits using loops. Basically, we need to know how to count how many digits in the number and then sum them up one by one.

One way to do that is to cast the variable containing the number to str to make it easier to iterate over.

num = 123 #The variable containing the number we want to sum its digits
num = str(num) #Casting the number to a str
s = 0 #Initialize a varible to accumulate the sum
#Loop over the digits and add them up
for i in range(len(num)):
  s += int(num[i])
# 2- Extract the parameters of your function.
Solving the problem using loops will help us understand the answer and figure out all the non-recursive aspects of it. Now that we have the answer, we can dissect it and extract the information we need to move on.

At this point, we need to ask ourselves a question, if I were to write this in a function form, what will the function parameters be?

The answer to this question depends on the programming language you are using. For Python, we can say that we only need one parameter, which is the variable num.

def sumOfDigitsIter(num):
    num = str(num)
    s = 0
    for i in range(len(num)):
        s += int(num[i])
    return s
# 3- Deduct minimal problem instance.
Once we get the function parameters, we are going to give them a deeper look. In our case, we only have one parameter that is num.

What we need to do now is find the minimal problem instance based on its parameters. To recall, our purpose was to sum the digits of a given number. The easiest instance of this problem is if the number only has one digit.

For example, if num = 3, then the answer will be equal to the variable itself since there are no more digits to add.

# 4- Add the solution to the minimal problem instance.
Let’s look again at the function we just wrote:

def sumOfDigitsIter(num):
    num = str(num)
    s = 0
    for i in range(len(num)):
        s += int(num[i])
    return s
Following this function's logic, if the parameter num is only one digit, the loop will still be executed. To avoid that, we can add a conditional statement that only executes if the number of digits in the input number is one.

def SumOfDigitsIter(num):
    num = str(num)
    if len(num) == 1:
      return num
    else:
      s = 0
      for i in range(len(num)):
          s += int(num[i])
      return s
# 5- Expand your function.
This is the step where recursion happens. Up until now, we didn’t care much about recursion; we were solving the problem logically. That’s the best approach to start with recursion, think about it logically, and then convert into a recursive solution.

Now, let’s consider the else section of our function.

[sourse](https://towardsdatascience.com/train-your-mind-to-think-recursively-in-5-steps-8f85c0e0eb81)

## Things I want to know more about


I want to learn about Think Recursively in python and Python Objects and Classes
