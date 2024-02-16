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