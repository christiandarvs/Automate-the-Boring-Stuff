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
- The regex ``(Ha){3,5}`` will match '**HaHaHa**', '**HaHaHaHa**', and '**HaHaHaHaHa**'.
- ``(Ha){3,}`` will **match three or more instances of the (Ha)** group, while ``(Ha){,5}`` will **match zero to five instances**. 
- Braces can help make your regular expressions shorter.
- A lot of use-cases

## Greedy and Non-Greedy Matching
- Python’s regular expressions are **greedy by default**, which means that in ambiguous situations **they will
match the longest string possible**.
- The **non-greedy** (also called lazy) version of the braces, which matches the
**shortest string possible**, has the closing brace followed by a question mark.
- Question Mark has two meanings: **declaring a non-greedy match** or **flagging an optional group**.

## ``findall()``
- ``search()`` - match object of the **first matched text** in the searched string.
- ``findall()`` - return the strings of **every match text** in the searched string.

## Character Classes
| Shorthand  | Represents  
|---|---|
| ``\d``  | Any numeric digit from **0 to 9**|
| ``\D``  | Any character that is **not a numeric digit from 0 to 9**|
| ``\w``  | Any letter, numeric digit, or underscore character. (**Matching "word" characters**)|
| ``\W``  | Any space, tab, or newline character. (**Matching "space" characters**)|
| ``\s``  | Any character that is not a space, tab, or newline|

## Caret and Dollar Sign Characters ``(^, $)``
- ``^`` - start of a regex to indicate that a **match must occur at the beginning of the searched text**.
- ``$`` - end of a regex to indicate that a **match must occur at the end of the searched text**.
- "Carrots cost dollars"

## The Wildcard Character
- The ``.`` **(or dot)** character in a regular expression is called a wildcard and will **match any character except for a newline**.

## Matching Everything with Dot-Star
- Dot character means **“any single
character except the newline”**
- Star character means **“zero or more of the preceding character.”**
- **Note**: The dot-star uses greedy mode

## Matching Newlines with the Dot Character
- The dot-star will match everything except a newline.
- ``re.compile(, re.DOTALL)`` - you can make the **dot character match all characters, including the newline character**

| Symbol  | What it does  
|---|---|
| ``?``  | matches zero or one of the preceding group|
| ``*``  | matches zero or more of the preceeding group|
| ``+``  | matches one or more of the preceeding group|
| ``{n}``  | matches exactly n of the preceeding group|
| ``{n, m}?`` or ``{*?}`` or ``{+?}`` | performs a non-greedy match of the preceeding group|
| ``^spam``  | means the string must begin with spam|
| ``spam$``  | means the string must end with spam|
| ``.``  | matches any character, except newline characters|
| ``\d``,``\w``, ``\s``  | match a digit, word, or space character, respectively|
| ``\D``,``\W``, ``\S``  | match anything except a digit, word, or space character, respectively|
| ``[abc]``  | matches any character between the brackets (such as ***a, b, or c***)|
| ``[^abc]``  | matches any character that is **not** between the brackets |

## Case-Insensitive Matching
- Sometimes you care only about matching the letters without worrying whether they’re uppercase or lowercase. 
- To make your regex case-insensitive, you can pass ``re.IGNORECASE`` or ``re.I`` as a **second argument** to ``re.compile()``

## Substituting Strings with the ``sub()``
- **1st argument** - string to replace any matches
- **2nd argument** - string for the RegEx."
- It returns a string with substitutions applied.

## Managing Complex RegExes
- Regular expressions are fine if the **text pattern you need to match is simple**. 
- Matching complicated text
patterns **might require long, convoluted regular expressions**.
- ``re.verbose()`` - function to ignore whitespace and comments inside the RegEx string.

## Combining <ins>integer constants</ins> within the ``re`` module
- ``some_regex_value = re.compile('foo', re.IGNORECASE | re.DOTALL | re.VERBOSE)``