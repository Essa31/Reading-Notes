# Dunder Methods
What are they? They are predefined methods that can be utilized in any class, they start and end with double underscores.

## Some examples on dunder methods and what they do:
Method	Used for

__init__	Defines the constructor of the class

__str__	Provides an informal string representation of the object

__repr__	Provides an official string representation of the object

.__len__	Provides the length, which is the number of items in the object

__getitem__	Returns the item that is in a specific index/position in the object

__reversed__	Iterates over the items within the object in a reversed order

__add__	Provides a way to perform 
operations on two object instances

__call__	Allows objects to be callable like regular functions

# Statistics - Probability
Probability is the chance for a certain event to happen, and in order to find that probability we need to rely on the statistics, which are data that comes from testing a bunsh of events to see their chance of occurring.

One of the ways to calculate the probability of an event to happen is using the normal distribution, which is a chape that shows how likely it is for an event to happen.





# Special Methods and the Python Data Model

Python data model lets devs tap into rich features like sequences, iteration, operator overloading, attribute access, etc.

Python’s data model is like a powerful API that you can interface with by implementing one or more dunder methods.

## Enriching a Simple Account Class
# Object Initialization:
to construct account objects from the account class you need a constructor which in Python is the init dunder.

The constructor takes care of setting up the object.

class Account: “"”A simple account class”””

def init(self, owner, amount=0): “”” This is the constructor that lets us create objects from this class “”” self.owner = owner self.amount = amount self._transactions = []

create new accounts like this: acc = Account(‘bob’) # default amount = 0 acc = Account(‘bob’, 10)
## Object Representation: str, repr
repr: the “official” string rep of an object. This is how you would an object of the class. The goal of repr is to be unambiguous.
str: the “informal” or nicely printable string rep of an object. This is the end-user. class Account:

def repr(self): return ‘Account({!r}, {!r})’.format(self.owner, self.amount)

def str(self): return ‘Account of {} with starting amount: {}’.format( self.owner, self.amount)

## Basic Statistics in Python – Probability
What is probability? seeks to answer the question, “what is teh chance of an event happening?. An event is some outcome of interest.
by looking at the events that can occur, probability gies us a framework for maing predictions about how often events will happen.
use stats to calculate probabilities based on observations from the real world and check how it compares to the ideal.


## Things I want to know more about

Dig deeper in the statistics methods