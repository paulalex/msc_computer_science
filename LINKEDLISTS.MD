# Linked List Data Structure

The linked list data structure is another type of dynamic set, like stack and queue, objects in a linked list are arranged in a linear order. Lists often maintain insertion order of elements added to them. Unlike an array where the linear order is determined by array indices, a linked lists order is maintained by a pointer to the next element in the list.

A linked list can take several forms, the list can be singly or doubly linked, it can be sorted or unsorted based on the keys and may or may not be circular. If the list is **singly linked** then the each element does not hold a *prev* pointer which references the element that comes before it, if the list is *sorted* then the order corresponds to the order of the keys stored in the list, if the list is **unsorted** then the elements can appear in any order.

If the list ic **circular** in nature then the *prev* pointer of the head elements points to the **tail** element and the *next* pointer of the tail element points to the *head* element and the list can be thought of as a *ring* of elements.

# Linked List Diagram

<p align="center">
  <img src="images/linked_list.PNG">
</p>

# Linked List Operations

## Search

The function *LIST-SEARCH(L, k)* below finds the first element in the list *L* with the key *k* using a linear search and then returns a reference to *k*, if no object matching *k* is found then the function returns *NIL*.

<p align="left">
  <img src="images/linked_list_search.PNG">
</p>

## Insert

<p align="left">
  <img src="images/linked_list_insert.PNG">
</p>

## Delete

<p align="left">
  <img src="images/linked_list_delete.PNG">
</p>

# List Sentinel

A list sentinel is a dummy object that allows the simplication of boundary conditions, a list *L* has an object *L.nil* that represents *NIL* but has all of the attributes of other elements in the list such as *next*, *previous* and whereever we previously had a reference to *NIL* in the code, we can now replace this with a reference to *L.nil*. The effect of this is that doubly linked list now becomes a **circular doubly linked list with sentinel**, where the sentinel *L.nil* lies between the *head* and the *tail* of the list. *L.nil.next* points to the head of the list, and *L.nil.previous* points to the tail of the list, this means any references to *L.head* can be removed.

<p align="center">
  <img src="images/linked_list_sentinel.PNG">
</p>

Sentinels rarely reduce the asymtotic time bounds of data structures but they do enable the simplification of code and can help to reduce constant factors in functions, often the gain from use of sentinels is one of clarity, rather than speed although in certain situations such as in a loop a sentinel can reduce the coefficient *n* with regard to running time.

Sentinels should be used sparingly, when there are many small lists the additional storage overhead of sentinels can lead to memory waste.

## Search with Sentinel

The code for the list search remains largely the same, with references *L.head* replaced with references to *L.nil*.

<p align="left">
  <img src="images/linked_list_search_sentinel.PNG">
</p>

## Insert with Sentinel

The code for the list insert remains largely the same, with references *L.head* replaced with references to *L.nil*.

<p align="left">
  <img src="images/linked_list_insert_sentinel.PNG">
</p>

## Delete with Sentinel

The code for list delete is simpler as boundary conditions can now be removed.

<p align="left">
  <img src="images/linked_list_delete_sentinel.PNG">
</p>
