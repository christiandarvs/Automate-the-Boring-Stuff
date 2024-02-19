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

## ``f-string``
- Common operation in programming
- ``print(f'User Name: {variable_name}')``