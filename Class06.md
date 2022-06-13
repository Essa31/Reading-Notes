# How to use the Random Module in Python


The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.

# When to use it?

When making your password database more secure or powering a random page feature of your website.

# Random functions
The Random module contains some very useful functions.

## Randint
If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.

import random
print random.randint(0, 5)
This will output either 1, 2, 3, 4 or 5.

## Random
If you want a larger number, you can multiply it.

For example, a random number between 0 and 100:

import random

random.random() * 100

## Choice

Generate a random value from the sequence sequence.

random.choice( ['red', 'black', 'green'] ).
The choice function can often be used for choosing a random element from a list.

import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]

random.choice(myList)
## Shuffle

The shuffle function, shuffles the elements in list in place, so they are in a random order.

random.shuffle(list) Example taken from this post on Stackoverflow

from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
Output:
 print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]

 of course your results will vary

## Randrange

Generate a randomly selected element from range(start, stop, step)


random.randrange(start, stop[, step])
import random

for i in range(3):

    print random.randrange(0, 101, 5)


## Code Example
Let’s see this example (copied from Doug Hellmann PYMOTW)

import random
import itertools

outcomes = { 'heads':0,
             'tails':0,
             }
sides = outcomes.keys()

for i in range(10000):
    outcomes[ random.choice(sides) ] += 1

print 'Heads:', outcomes['heads']
print 'Tails:', outcomes['tails']
There are only two outcomes allowed, so rather than use numbers and convert them, the words “heads” and “tails” are used with choice().
[11:50 AM]
The results are tabulated in a dictionary using the outcome names as keys.

$ python random_choice.py

Heads: 4984
Tails: 5016


# Risk Analysis

# What is Risk Analysis in Software Testing and how to perform it?
risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test.

# Why use Risk Analysis?

using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks.

# Risk magnitude indicators
High: means the effect of the risk would be very high and non-tolerable. The company might face loss.

Medium: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.

Low: it is tolerable. There lies little or no external exposure or no financial loss.

# Risk Identification

Business Risks

Testing Risks

Premature Release Risk

Software Risks

# The perspective of Risk Assessment

Effect – To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.

Cause – To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.

Likelihood – To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.

# How to perform Risk Analysis?
Searching the risk

Analyzing the impact of each individual risk

Measures for the risk identified

# Dependency Injection
## What is Dependency Injection?

Is a technique whereby one object (or static method) supplies the dependencies of another object. A dependency is an object that can be used (a service).

## Small Definition: Dependency or dependent means relying on something for support

## Why should I use dependency injection?
We can think of DI as the middleman in our code who does all the work of creating the preferred tasks object and providing it to our class.

#Types of dependency injection:
constructor injection: the dependencies are provided through a class constructor.
setter injection: the client exposes a setter method that the injector uses to inject the dependency.
interface injection: the dependency provides an injector method that will inject the dependency into any client passed to it.
## Dependency Injection’s Responsibility
Create the objects

Know which classes require those objects

And provide them all those objects

## Inversion of control —the concept behind DI

This states that a class should not configure its dependencies statically but should be configured by some other class from outside.

## Benefits of using DI

Helps in Unit testing.

Boiler plate code is reduced, as initializing of dependencies is done by the injector component.

Extending the application becomes easier.

Helps to enable loose coupling, which is important in application programming.

## Disadvantages of DI
It’s a bit complex to learn, and if overused can lead to management issues and other problems.

Many compile time errors are pushed to run-time.
Dependency injection frameworks are implemented with reflection or dynamic programming. This can hinder use of IDE automation, such as “find references”, “show call hierarchy” and safe refactoring.
## Libraries and Frameworks that implement DI
Spring (Java)

Google Guice (Java)

Dagger (Java and Android)

Castle Windsor (.NET)

Unity(.NET)

# Resources

[sources](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

[sources](https://www.edureka.co/blog/risk-analysis-in-software-testing/)

[sources](https://martinfowler.com/bliki/TestCoverage.html)


