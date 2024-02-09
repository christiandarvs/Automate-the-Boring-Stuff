# Chapter 4 - Lists
## List Data Type

- Contains multiple value in an ordered sequence. It can store a variable or passed to a function. 
- Values inside the the list are called **items** or **elements**.

## Getting Individual Values in a List with Indexes
- **Indeces** are used to access an element in a list. It must be an Integer. 
- **Index Error** - This occurs when we use an index that exceeds the length of the list.
- **Negative Indeces** - We can start from the end/last by providing ``-1`` as its index.
- **Index Slicing** - In a slice, the **first integer** is the index where the slice **starts**. The **second integer** is the index where the slice **ends**. A slice goes up to, but will not include, the value at the second index. A slice evaluates to a new list value.

## Getting a List's Length with ``len()``
- ``len()`` - returns the number of elements that are in a list value passed to it. The function can also count the number of characters in a string value.

## Changing Values in a List with Indexes
- ``list_variable[index] = new value``

## Concatenation and Replication
- **Concatenation** - use the ``+`` operator. It is useful when creating a new list by combining two lists.
- **Replication** - use the ``*`` operator outside the list. It is useful when you have the same elements.

## Removing Values from Lists with ``del`` Statements
- The del statement will delete values at an index in a list. All of the values in the list after the deleted value
will be moved up one index.