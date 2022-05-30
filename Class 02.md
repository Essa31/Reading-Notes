# Unit tests ?

Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.

# (TTD) Test-Driven Development in Python


Test-driven development (TDD) is a process that has been documented considerably over recent years. A process of baking your tests right into your everyday coding, as opposed to a nagging afterthought, should be something that developers seek to make the norm, rather than some ideal fantasy.

This approach allows you to escape the trap that many developers fall into.

TDD, in its most basic terms, is the process of implementing code by writing your tests first, seeing them fail, then writing the code to make the tests pass. You can then build upon this developed code by appropriately altering your test to expect the outcome of additional functionality, then writing the code to make it pass again.

# Example Problem and Test-Driven Approach


We are going to take a look at a really simple example to introduce both unit testing in Python and the concept of TDD. We will write a very simple calculator class, with add, subtract and other simple methods as you would expect. 

import unittest
 
class TddInPythonExample(unittest.TestCase):
 
    def test_calculator_add_method_returns_correct_result(self):
        calc = Calculator()
        result = calc.add(2,2)
        self.assertEqual(4, result)



[sourse](https://code.tutsplus.com/tutorials/beginning-test-driven-development-in-python--net-30137)

# What does the if __name__ == “__main__”: do?

Before executing code, Python interpreter reads source file and define few special variables/global variables. 
If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value “__main__”. If this file is being imported from another module, __name__ will be set to the module’s name. Module’s name is available as value to __name__ global variable. 

A module is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended. 

## Python program to execute
## main directly


print ("Always executed")

if __name__ == "__main__":

    print ("Executed when invoked directly")

else:

    print ("Executed when imported")

# Recursion

## What is Recursion? 

The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called a recursive function. Using a recursive algorithm

## Need of Recursion

Recursion is an amazing technique with the help of which we can reduce the length of our code and make it easier to read and write. It has certain advantages over the iteration technique which will be discussed later. A task that can be defined with its similar subtask, recursion is one of the best solutions for it. For example; The Factorial of a number.

## An example of direct recursion
void directRecFun()
{
    // Some code....

    directRecFun();

    // Some code...
}

// An example of indirect recursion
void indirectRecFun1()
{
    // Some code...

    indirectRecFun2();

    // Some code...
}
void indirectRecFun2()
{
    // Some code...

    indirectRecFun1();

    // Some code...
}

How memory is allocated to different function calls in recursion? 
When any function is called from main(), the memory is allocated to it on the stack. A recursive function calls itself, the memory for a called function is allocated on top of memory allocated to calling function and different copy of local variables is created for each function call. When the base case is reached, the function returns its value to the function by whom it is called and memory is de-allocated and the process continues.
Let us take the example how recursion works by taking a simple function. 

// A Java program to demonstrate working of
// recursion
class GFG {
    static void printFun(int test)
    {
        if (test < 1)
            return;
        else {
            System.out.printf("%d ", test);
            printFun(test - 1); // statement 2
            System.out.printf("%d ", test);
            return;
        }
    }
 
    // Driver Code
    public static void main(String[] args)
    {
        int test = 3;
        printFun(test);
    }
}
 
// This code is contributed by
// Smitha Dinesh Semwal
Output : 

3 2 1 1 2 3


# Python List

Lists are used to store multiple items in a single variable.

Lists are one of 4 built-in data types in Python used to store collections of data, the other 3 are Tuple, Set, and Dictionary, all with different qualities and usage.

Lists are created using square brackets:

Example

Create a List:

thislist = ["apple", "banana", "cherry"]
print(thislist)

OUTPUT: ['apple', 'banana', 'cherry']

Ordered.
Not Fixed Values.
Allow duplicate.
Indexed.
Not Fixed size.
[].

# Modules and Packages

its python file contain variables ,methods and classes.

module can be added to your project.
module extension is “.py”.

The benefit of module is to make the code use more than one time.

In large projects, the work must be divided into a group of modules, which helps in organization and development and maintenance easy in the future.

Import built-in Modules:

1-import math

print('pow(5,2)= ',math.pow(5,2)) output: 10

2-import platform
print('os: ',platform.system()) output: os:  Windows

3-import datetime

sysdate=datetime.datetime.now()

print(sysdate)

output: 

2021-12-23 10:46:33.345207
4-import calendar 

calendar.prcal(2018)

to start new module :

		File -->  new File

Then write the next method:

	def sum_two_num(n1,n2):

		return n1+n2

save file (sum_fun.py)
 
make another module :

		File -->  new File

Then write the next method:

def avg_fun (n1,n2):

        avg_val=sum_two_num(n1,n2)/2
        return avg_val

print(avg_fun(5,9))
Run File
 
make another module :

Then write the next method:

import sum_fun

def avg_fun (n1,n2):

        avg_val=sum_fun.sum_two_num(n1,n2)/2
        return avg_val
print(avg_fun(5,9))
Run File
 
Output:
7.0

# python string

pytest: helps you write better programs
The pytest framework makes it easy to write small, readable tests, and can scale to support complex functional testing for applications and libraries.

A quick example
content of test_sample.py

def inc(x):
    return x + 1


def test_answer():
    assert inc(3) == 5

To execute it:

$ pytest

=========================== test session starts ============================

platform linux -- Python 3.x.y, pytest-7.x.y, pluggy-1.x.y

rootdir: /home/sweet/project
collected 1 item

test_sample.py F                                                     [100%]

================================= FAILURES =================================
_______________________________ test_answer ________________________________

        assert inc(3)==5
E       assert 4 == 5

E        +  where 4 = inc(3)

test_sample.py:6: AssertionError
========================= short test summary info ==========================
FAILED test_sample.py::test_answer - assert 4 == 5
============================ 1 failed in 0.12s =============================
Due to pytest’s detailed assertion introspection, only plain assert statements are used. See Get started for a basic introduction to using pytest.

# pytest documentation


[pytest documentation](https://docs.pytest.org/en/latest/contents.html)

# Pytest Parallel

Run Tests in Parallel with Pytest
Usually, a test suite will have multiple test files and hundreds of test methods which will take a considerable amount of time to execute. Pytest allows us to run tests in parallel.

For that we need to first install pytest-xdist by running

pip install pytest-xdist

You can run tests now by

py.test -n 4
-n <num> runs the tests by using multiple workers. In the above command, there will be 4 workers to run the test.

## Things I want to know more about

I want to learn about lists in python