# Chapter 6 - Manipulating Strings

## Escape Characters
- An escape character lets you use characters that are otherwise impossible to put into a string. An escape character consists of a ``backslash (\)`` **followed by the character you want to add to the string**. (Despite consisting of two characters, it is commonly referred to as a singular escape character.)

| Escape Character  | Prints as  
|---|---|
| ``\'``  | Single quote  |
| ``\"``  | Double quote  |
| ``\t``  | Tab  |
| ``\n``  | Newline (line break) |
| ``\\``  | Backslash  |

## Raw Strings
- You can place an `r` **before the beginning quotation mark** of a string to make it a raw string. A **raw string completely ignores all escape characters** and prints any backslash that appears in the string.
- Python considers the backslash **as part of the string** and not as the start of an escape character.
- Raw strings are helpful if you are typing string values that contain many backslashes, such as the strings used for **Windows file paths** like ``r'C:\Users\Coder\Desktop'`` or **regular expressions**

## Indexing and Slicing Strings
- **Strings use indexes and slices** the same way lists do. You can think of the string 'Hello, world!' as a list and each character in the string as an item with a **corresponding index**.
- If you specify an index, you’ll get the **character at that position in the string**. If you specify a range from one index to another, **the starting index is included and the ending index is not.**
- This is similar to how range(5) will cause a for loop to iterate up to, **but not including, 5**.
- **Note**: slicing a string does not modify the original string. You can capture a slice from one variable in a separate variable.

## The ``in`` and ``not in`` Operators with Strings
- can be used with strings just like with list values. An expression with two strings joined using in or not in will evaluate to a Boolean ``True`` or ``False``
- These expressions test whether the first string (**the exact string**, **case-sensitive**) can be found within the second string.

## ``f-string (string-interpolation)``
- Common operation in programming, used for concatenation
- ``print(f'User Name: {variable_name}')``

## ``upper()`` and ``lower()``
- The upper() and lower() string methods return a new string where all the letters in the original string have been converted to **uppercase or lowercase**, respectively.

## ``isupper()`` and ``islower()``
- The ``isupper()`` and ``islower()`` methods will return a Boolean ``True`` value if the string has **at least one letter** and **all the letters are uppercase or lowercase**, respectively.

## ``isX()`` Methods
- ``isalpha()``: Returns True if the string consists only of letters and isn’t blank
- ``isalnum()``: Returns True if the string consists only of letters and numbers and is not blank
- ``isdecimal()``: Returns True if the string consists only of numeric characters and is not blank
- ``isspace()``: Returns True if the string consists only of spaces, tabs, and newlines and is not blank
- ``istitle()``: Returns True if the string consists only of words that begin with an uppercase letter followed by
only lowercase letters
- helpful when you need to validate user input.

## ``startswith()`` and ``endswith()``: **case-sensitive**
- The ``startswith()`` and ``endswith()`` methods return ``True`` if the string value they are called on **begins or ends (respectively) with the string passed to the method**; otherwise, they return ``False``.

## ``join()`` and ``split()``
- The ``join()`` method is useful when you have a list of strings that need to be joined together into a single string value.
- called on a string, gets passed a list of strings, and returns a string. The **returned string is the concatenation of each string in the passed-in list**
- The ``split()`` method does the opposite: It’s called on a string value and **returns a list of strings**.

## Splitting Strings with the ``partition()`` Method
- can split a string into the text **before** and **after** a separator string. 
- This method searches the string it is called on for the separator string it is passed, and returns a tuple of three substrings for the **“before,” “separator,”** and **“after”** substrings.
- The ``partition()`` method is useful for **splitting a string** whenever you need the parts **before, including, and after a particular separator string**.

## ``rjust()``, ``ljust()``, and ``center()``
- The ``rjust()`` and ``ljust()`` string methods return a padded version of the string they are called on, with spaces inserted to justify the text.
- The ``center()`` - centers the text rather than justifying it to
the left or right.
- **1st Parameter**: is an integer length for the justified string.
- **2nd Parameter** (Optional): will specify a fill character other than a space character.
- These methods are especially useful when you need to print tabular data that has correct spacing.

## ``rstrip()``, ``lstrip()``, and ``strip()``