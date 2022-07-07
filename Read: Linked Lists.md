# Read: Linked Lists

## Big O: Analysis of Algorithm Efficiency

When and why do we use the **Big O notation** ?

We use the **Big O notation** whenever we need to represent an algorithm or function's efficiency, and In order to do that we need to measure the **Time and Space complexity**.

Ok so what is the **Time and Space complexity**? Well lets start with the **Time complexity** :

- It is the amount of time that a function needs to complete all it's processes 

As for the **Space complexity**:

- It is the amount of storage that function needs to store its data

**Notes**: 

- There are a couple of ways to measure the Time complexity:
    - It can be measured using **milliseconds**, from the start of executing a function until it finishes.
    - It can be measured by the number of executed **Operations**.
    - It can be measured by the number of executed **Basic Operations**.

- The sources of memory Usage during the run-time of the function:
    - Space for holding the **algorithm code**
    - Space for holding the **input data**
    - Space for holding the **output data**
    - Space for holding the **working space**

## Linked Lists

### ***Definition***: 

A **Liked List** is series of connected **Nodes**(*items*), where each one of them at least reference the next **node** in line.

### ***Types of Linked Lists***:

There are two types of liked lists:
- **Singly linked list**: It's where each node points to the next one in line.
- **Doubly linked list**: It's where each node points to the next and previous node.

**Note**: There are some important terms when it comes to linked lists and these are:
- *Head*: it refers to the start of the linked list.
- *current*: it refers to, you guessed it, the current point of that we are at. (When creating a linked list the current == Head at the start)

### ***Traversing the Linked List***:

In order to traverse a linked list we need to relay on the pointers(the **next** values), and by using a **while loop** we can go through them as long as we don't we have a pointer.

**Note**: The **current** pointer/variable helps us to know were are we in the linked list.


### ***Adding a New Node***

Adding a new node is pretty simple, *first* we need to create a new node, *then* we need to assign a value to it, *after that* we need to make the **"next" pointer** equal to the current **"Head" pointer**, and finally we need to re-assign the **"Head" pointer** in the linked list which is now the new node we just added

```
    create newNode          #1
    newNode.Value = value   #2
    newNode.Next = Head     #3
    Head = newNode          #4
```

### ***Some of The Great Characteristics of Linked lists***

- Linked list is a **linear data structures**: this means that they are a great choice for many problems as they have a great time and space complexity.(mostly O(n))
- Memory and Space management: as much as our machines are strong now a days, we still need to manage the memory for some programs, and linked lists are one of the good choices for that, because it doesn't need to locate a specific block for all the data, as it scatters them where ever the memory finds free space.
- Linked lists works for almost all shapes and sizes: the reason behind that is the types of linked lists we have, where according to the situation you can either use **Singly** or **Doubly** linked list.

## Resources

[sources1](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

[sources2](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)