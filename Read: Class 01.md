# Why Big O?

It’s very important for interviews and you need it to get that job! Other than that it provides a vocabulary to talk about how our code is performing and to decide which approach to take to solve a problem.

![](https://hackernoon.com/_next/image?url=https%3A%2F%2Fhackernoon.com%2Fimages%2F3caCsLpQ3zZrK5b6kqoOFy7Vatw1-af8l32l4.jpg&w=1920&q=75)

# type of  Big O :

## O(1)
The first Big O Notation that we have is O(1), it simply means that the operation will always execute in a constant amount of time regardless of how big the input size is.

## O(n)
Let me introduce you to the most common Big O Notation, the O(n) notation, let us see this with the help of an example.

## O(N^2)
Remember O(n), the number of operations it performs scales in direct proportion to the input.

In the case of O(n^2), the number of operations it performs scales in proportion to the square of the input. This is common with algorithms that involve nested loops or iterations.

## O(2^n)
We are entering dangerous waters here, in interviews and in implementation we want to avoid a situation where the time complexity of our algorithm reaches O(2^n) as it denotes an algorithm whose growth doubles with each addition to the input data set.

## O(log n)
Now we haven’t touched the logarithms yet, and that’s because they are slightly tricky to understand. We usually encounter log when we are searching through data sets.

[Sourse](https://hackernoon.com/a-beginners-guide-to-the-big-o-notation-yb7332wf)

# Pain vs. Suffering

It may be difficult to differentiate between pain and suffering for some people, but if you look closely, you will find it easy.

1. You’ll be pushed mentally, having to think your way through problems that you had only even heard about a few hours beforehand.
2. You’ll have to forge your own path toward a solution.
3. You’ll have to research for hours on end, fleshing out the skeleton that we discuss in class, piling information on top of application so that you can reach your goals.

# Names and Values in Python

1. what is python: -It is a programming language, rather it is one of the most important programming languages that are currently used.

2. why should we learn it: and one of the reasons for learning it is its ease of use compared to other languages

3. variables: When we define variables, the value of the variable is reserved in RAM, and the storage capacity changes according to the data type, such as: 1-integer. 2-float. 3-string.

4.  Naming rules: a- not keyword. b- a-z, A-Z, 0-9 , _ . c- must start with character

5. resrved words: *- if, else, class, while , for, print ,break, continue, elif.
6. how to define variables: How to define variables:
X=0
If a variable is defined and starts with a number, it will give  error ex:
1x=0                                                  output:    Syntax Error: invalid syntax

7. How to determine the type of a variable?  ex: X=0   output:    <class 'int'> Print(type(x))

task  : write a python program that accept a list and return the number of words that has more than 2 characters and the first letter same as the last letter .

ex:

 words =['abc','aba','cd','123','1221']

solution :

words =['abc','aba','cd','123','1221']

counter=0

for i in words :

    if len(i)>2 and i[0] == i[-1] :
        print(i)
        counter+=1
else :

    print(counter)


## Things I want to know more about

I want to dive deeper into OOP in python to become  professional at AI.