# Read: Hash Tables

## Definition

HashTables or HashMaps are a type of abstract data, that can be used to map keys to values.

### Some basic terminologies:

- **Hash** is a result of an converting a string into another value.
- **Buckets** are the reference the values contained within the indexes of the array.
- **Collisions** are when more than one key is hashed to the same location within a hashtable.

**Note**: 

- Hash maps have a read access of *O(1)*
- Hash code turns keys into integers

### Creating a Hash:

In order to create a hash you need to:

- Calculate the ASCII code of all the letters in the key, and add them together.
- Multiply the result with a prime number.
- Divide the result by the total size of the array (*1024*)
- Insert into the array by using the result as an index.

ex: ([source](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html))

    Key = "Cat"
    Value = "Josie"

    67 + 97 + 116 = 280

    280 * 599 = 69648

    69648 % 1024 = 16

    Key gets placed in index of 16. 

### Collisions:

As mentioned before collisions are when two values hash to the same index, which is a problem, as they would override eachother, and in order to solve this problem we need to change the initial state of the buckets from `null` to `LinkedList`, which would lead to collisions becoming nodes within that linked list.

**Note**: when storing within a linked list it is important to store not just the value, but the key as well, so we can call the value by it's key.


## Resources

[sources1](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

[sources2](https://www.youtube.com/watch?v=MfhjkfocRR0)

[sources3](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)