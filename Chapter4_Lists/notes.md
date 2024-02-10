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
- ``del`` ``list_name[index]``

## Using for Loops with Lists
- A common Python technique is to use ``range(len(someList))`` with a for loop to iterate over the indexes of a list.
- Using ``range(len(supplies))`` in the previously shown for loop is handy because the code in the loop can access the index (as the variable ``i``) and the value at that index (as supplies``[i]``). Best of all, ``range(len(supplies))``
will iterate through all the indexes of supplies, no matter how many items it contains.

## The ``in`` and ``not`` in operators
- You can determine **whether a value is or isn’t in a list** with the ``in`` and ``not in`` operators. 
- Like other operators, in and not in are used in expressions and connect two values: a value to look for in a list and the list where it may be found. 
- These expressions will evaluate to a **Boolean value**.

## Multiple Assignment Trick
- Technically called ***tuple unpacking*** is a shortcut that lets you assign multiple variables with the values in a list in one line of code