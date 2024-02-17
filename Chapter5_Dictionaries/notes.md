## Dictionary Data Type
- In List and Tuple, we used index to access elements. However, in Dictionary we use **Key**.
- To retrieve the **keys**, use ``.keys()``
- To retrieve the **values**, use ``.values()``
- They can’t be sliced like lists.
- Trying to access a key that does not exist in a dictionary will result in
a ``KeyError`` error message.

## Dictionaries vs. Lists
- Lists - are ordered, **THERE IS** a first element.
- Dictionaries - are unordered, **THERE IS NO** first element.

## ``keys()``, ``values()``, and ``items()`` Methods
- When you use the ``keys()``, ``values()``, and ``items()`` methods, a ``for loop`` can iterate over the **keys**, **values**, or **key-value pairs** in a dictionary, respectively. Notice that the values in the dict_items value returned by the ``items()`` method are **tuples of the key and value**.
- Multi-assignment using ``.items()`` *(Refer to code-implementation)*

## ``get()`` Method
- It’s tedious to check whether a key exists in a dictionary before accessing
that key’s value. 
- Fortunately, dictionaries have a ``get()`` method that takes
**two arguments**: the **key of the value to retrieve** and a **fallback value to
return if that key does not exist**.
- ``dictionary_variable.get('key', fallback_value)``
- The fallback value can be an any data type

## ``setdefault()`` Method
- The ``setdefault()`` method offers a way to do this in one line of code.
- **1st argument**: is the key to check for
- **2nd argument**: is the value to set at that key if the key doesn't exist.
- If the key does exist, the ``setdefault()`` method returns the key’s value.
- The ``setdefault()`` method is a nice shortcut **to ensure that a key exists**.

## Pretty Printing - (**Module**)
- If you import the ``pprint`` module into your programs, you’ll have access
to the ``pprint()`` and ``pformat()`` functions that will “pretty print” a
dictionary’s values. This is helpful when you want a cleaner display of the items in a dictionary than what ``print()`` provides.
- The ``pprint.pprint()`` function is especially helpful when the dictionary
itself contains **nested lists or dictionaries**.
- If you want to obtain the **prettified text as a string value** instead of
displaying it on the screen, call ``pprint.pformat()`` instead.

## Nested Dictionaries and Lists
- Lists are useful to contain an **ordered series of values**, and dictionaries are useful for **associating keys with values**.
- Inside the loop, the string of the guest’s name is assigned to ``key``, and the **dictionary of picnic items** they’re bringing is assigned to ``value``. If the item parameter exists as a key in this dictionary, its value (the quantity) is added to ``numBrought``. If it does not exist as a key, the ``get()`` method **returns 0** to be added to ``numBrought``.
- **Explanation**: This may seem like such a simple thing to model that you wouldn’t need to bother with writing a program to do it. But realize that this
same ``total_brought()`` function could easily handle a dictionary that contains thousands of guests, each bringing thousands of different picnic items. Then having this information in a data structure along with the ``total_brought()`` function would save you a lot of time!

## Summary:
- Lists and dictionaries are data types that can contain multiple values, including other lists and dictionaries.
- Dictionaries are useful because **you can map one item (the key) to another (the value)**.
- Values inside a dictionary are accessed using square brackets just as with lists. Instead of an integer index, **dictionaries can have keys of a variety of data types: integers, floats, strings, or tuples.**