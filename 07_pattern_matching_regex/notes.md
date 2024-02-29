## Regular Expressions
- **Regular expressions,** called *regexes* for short, are **descriptions for a pattern of text**. For example, a ``\d`` in a
regex stands for a digit character—that is, any single numeral from 0 to 9.

## Matching Regex Objects
- ``search()``- searches the string it is passed for any matches to the regex. It will return ``None`` if the regex pattern is not found in the string. If the pattern is found, the ``search()`` returns a Match object, which have a ``group()`` that will return the actual matched text from the searched string.

## Review of Regular Expression Matching
1. Import the regex module with import re.
2. Create a Regex object with the re.compile() function. (Remember to use a raw string.)
3. Pass the string you want to search into the Regex object’s search() method. This returns a Match object.
4. Call the Match object’s group() method to return a string of the actual matched text.

## Special Meanings:
- If you want to detect these characters as part of your text pattern, you need to escape them with a backslash: ``\.`` ``\^`` ``\$`` ``\*`` ``\+`` ``\?`` ``\{ \}`` ``\[ \]`` ``\\`` ``\|`` ``\( \)``

## Matching Multiple Groups with the Pipe
- The ``|`` character is called a **pipe**. You can use it anywhere you want to match one of many expressions. For
example, the regular expression`` r'Batman|Tina Fey'`` will match either ``'Batman'`` or ``'Tina Fey'``.