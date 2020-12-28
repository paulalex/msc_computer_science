# Hash Tables and direct addressing

## Direct Address Tables

A direct address table is a type of data structure that maps records to values in an array using a key value which is **hashed** to represent some element in a corresponding array. Direct addressing enables fast insertion, retrieval and deletion operations on data items.

Direct addressing is a technique that works well when the **universe** of potential keys is reasonably small:

`U = {0, 1, ..., m-1}`

Generally we also assume that ***no two elements have the same key*** and to represent the dynamic set we use an array (also called a **direct address table**), represented as:

`T[0, 1, ..., m-1]`

An array can be built `T[0...m-1]`, where an element with key ***k*** is placed at `T[k]` and `T[i] = NIL` if there is no element in the data structure with the key ***i***.

In the following diagram each position or slot in the table ***T***, corresponds to a key in the universe ***U***.

<p align="left">
  <img src="images/direct_address_table.PNG">
</p>

Direct address tables support the following functions:

* SEARCH in **O(1)** time
* INSERT  in **O(1)** time
* DELETE in **O(1)** time

## Hash Tables

When the number of keys that need to be held as part of the data structure are large it becomes impractical to use a direct address table, and instead it becomes more feasible to use a hash table.

A hashtable is a data structure that allows for very fast retrieval of data, regardless of how much data there is. Hashtables are widely used in caching and database indexing.

## Hashing Algorithm

A hashing algorithm is a calculation applied to a key to transform it into an address. For example a numeric key can be divided by the number of available addresses ***n*** and the remainder can be used as the index value.

For alphanumeric keys the sum of the ASCII code values of the characters that make up the key can be divided by the number of available addresses ***n*** and the remainder can be used as the index value.

Another method that can be used is **folding** where a number such as a telephone number of 01452 8345654 becomes `01 + 45 + 28 + 34 + 56 + 54 = 218` and this may then be divided by some constant ***c*** and the remainder used as the index value.

Hashing algorithms will always have the potential to generate the same hashcode for a different key, and when this happens a ***collision*** occurs

## Collisions

### Open Addressing

### Closed Addressing

#### Linear Probing

#### Quadratic Probing

#### Double Hashing
