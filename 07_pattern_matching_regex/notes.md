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

## Optional Matching with the Question Mark ``?``
- The ``?`` character flags the group that precedes it as an **optional part of the pattern**.
- The ``(wo)?`` part of the regular expression means that the **pattern wo is an optional group**. The regex will match text that has zero instances or one instance of wo in it. This is why the regex matches both ``'Batwoman'`` and ``'Batman'``.
- Using the earlier phone number example, you can make the regex look for phone numbers that do or do not have an area code.
- You can think of the ``?`` as saying, “**Match zero or one of the group preceding this question mark**.” If you need to match an actual question mark character, escape it with ``\?``.

## Matching Zero or More with the Star
- The ``*`` (called the star or asterisk) means “**match zero or more**”—the group that precedes the star can occur any number of times in the text. It can be completely absent or repeated over and over again.
- If you need to match an actual star character, prefix the star in the regular expression with a backslash,``\*``.

## Matching One or More with the Plus
- While ``*`` means “**match zero or more**,” the ``+`` (or plus) means “**match one or more**.” Unlike the star, which does not require its group to appear in the matched string, the group preceding a plus **must appear at least once. It is not optional.**
- The regex Bat(wo)+man will not match the string 'The Adventures of Batman', because at least one wo is required by the plus sign.
- If you need to match an actual plus sign character, prefix the plus sign with a backslash to escape it: ``\+``.

## Matching Specific Repetitions with Braces
- 