
# Dynamic Sets

Mathematical sets are static while sets in Computer Science are dynamic. Elements in a set are represented by an object (say **x**) and an object contains a key field (say **k**) and some *satellite data*. General operations on a dynamic set **S** include:

* SEARCH (S, k)
* INSERT (S, x)
* DELETE (S, x)
* MINIMUM (S)
* MAXIMUM (S)
* SUCCESSOR (S, x)
* PREDECESSOR (S, x)

## Satellite Data

Satellite data is nothing more than additional data that forms part of an object in a dynamic set, if **k** is the key value in some arbitrary object, and it is this field that is used for sorting purposes then satellite data represents the other properties of this object, other than **k**.

In the following example in C, the key is the **id** field, whilst the fields age and name are satellite data:

```C
struct {
  int id;
  int age;
  char name[50];  
}
```

# Stack Data Structure

The stack data structure is a type of **dynamic set** and a deleted element is the most recent element that has been added to the stack, stacks operate in the sense of real life stacks using a **first in first out** policy. For example a stack of plates where new plates are placed on top, and the most recently added plate (the top plate) is the first to be removed when a new plate is required.

The insert operation on a stack is commonly called a **PUSH** operation and the delete operation on a stack is commonly called a **POP** operation.


