# Regular Expressions [re]:

In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import
import re
Basic Patterns: Ordinary Characters
You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.
Examples are 'A', 'a', 'X', '5'.
Wild Card Characters: Special Characters
Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.
-    . - A period. Matches any single character except the newline character.
-    ^ - A caret. Matches the start of the string.
-    $ - Matches the end of string.
-    [abc] - Matches a or b or c.
-    [a-zA-Z0-9] - Matches any letter from (a to z) or (A to Z) or (0 to 9).
-    \ - Backslash. Perhaps, the most diverse metacharacter!!
If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1) Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through (Scenario 2). \ can be used in front of all the metacharacters to remove their special meaning (Scenario 3).
function provided by ‘re’
    compile(pattern, flags=0)
    With compile(), you can computer a regular expression pattern into a regular expression object. When you need to use an expression several times in a single program, using compile() to save the resulting regular expression object for reuse is more efficient than saving it as a string. This is because the compiled versions of the most recent patterns passed to compile() and the module-level matching functions are cached.
    search(pattern, string, flags=0)

    With this function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match. It returns a corresponding match object if found, else returns None if no position in the string matches the pattern. Note that None is different from finding a zero-length match at some point in the string.
        match(pattern, string, flags=0)

    Returns a corresponding match object if zero or more characters at the beginning of string match the pattern. Else it returns None, if the string does not match the given pattern.
        findall(pattern, string, flags=0)

    similar to findall() - it finds all the possible matches in the entire sequence but returns regex match objects as an iterator.
        sub(pattern, repl, string, count=0, flags=0)

    sub() is the substitute function. It returns the string obtained by replacing or substituting the leftmost non-overlapping occurrences of pattern in string by the replacement repl. If the pattern is not found, then the string is returned unchanged.
        subn(pattern, repl, string, count=0)

    This splits the strings wherever the pattern matches and returns a list. If the optional argument maxsplit is nonzero, then the maximum ‘maxsplit’ number of splits are performed.
        start() - Returns the starting index of the match.
        end() - Returns the index where the match ends.
        span() - Return a tuple containing the (start, end) positions of the match.

# shutil — High-level File Operations:
Purpose:	High-level file operations.
The shutil module includes high-level file operations such as copying and archiving.
