# List Comprehensions in Python

The syntax for creating a list comprehension is:

the_list_name = [ expression for item in list]

List Comprehension is a more compact, flexible and faster than other methods of creating, looping and managing lists.


## Some Examples on Creating a List Comprehension
Creating a list with range() examples:
------------------------------------

numbers = [num for num in range(20)]
print(numbers)

------------------------------------

squares = [squ**2 for squ in range(20)]
print(squares)

------------------------------------

multiple_three = [ mult*3 for mult in range(20) ]
print(multiple_three)

------------------------------------
## List comprehensions with condition example:
even_nums = [ num for num in range(1,20) if num % 2 == 0]
## Parsing a file using list comprehension example:
file = open("text_file.txt", 'r')

txt = [ line for line in file ]

for line in txt:
    print(line)
## Using functions in list comprehensions example:
def multi(num):
    return x*2

nums = [multi(num) for num in range(1,20)]
print(nums)


 ## Show the first letter of each word using Python
So far we’ve seen examples of building a list of numbers in Python. Next, let’s try working with strings and the various ways list comprehensions can be used to elegantly handle a list of strings.

Example 4: Using list comprehensions with strings :
#a list of the names of popular authors

authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]


 #create an acronym from the first letter of the author's names

letters = [ name[0] for name in authors ]
print(letters)

Output

['E', 'L', 'F', 'T', 'E', 'S']
## Lower/Upper case converter using Python :

Using list comprehension to loop through a string in Python, it’s possible to convert strings from lower case to upper case, and vice versa.

Example 5: Changing a letter’s case

lower_case = [ letter.lower() for letter in ['A','B','C'] ]
upper_case = [ letter.upper() for letter in ['a','b','c'] ]

print(lower_case, upper_case)

Output

['a', 'b', 'c'] ['A', 'B', 'C']




## Things I want to know more about
None


## Resources

[sources1](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

[sources2](https://www.w3schools.com/python/python_lists_comprehension.asp)

[sources3](https://www.programiz.com/python-programming/list-comprehension)

