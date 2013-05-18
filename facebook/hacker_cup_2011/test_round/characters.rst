Characters
==========

You're interested in figuring out the number of case-insensitive unique
characters in some string. This sounds simple and easily-automated, so you just
decide to just go for it.

Input
-----

Your input will consist of an integer **N** followed by a newline. **N** test
cases will follow, all separated by newlines. Each test case is a string of
letters containing some combination of letters (upper- and lower-case are
allowed), the space character, and the characters contained in the string
**?!.'$%&*:;,.**

Output
------

Your output should consist of one integer per case, separated by whitespace,
indicating the number of case-insensitive unique characters contained in the
input string.

Constraints
-----------

5 ≤ **N** ≤ 25

Input strings will not exceed 100 characters in length.

Example input
-------------

::

    5
    Lorem ipsum
    Eclipse is a pretty nice editor.
    This is not a very interesting case.
    The quick brown fox jumps over the lazy dog
    Bonk.

Example output
--------------

::

    Case #1: 10
    Case #2: 15
    Case #3: 15
    Case #4: 27
    Case #5: 5

`View online <https://www.facebook.com/hackercup/problems.php?pid=193751083968425&round=103456299728530>`_.
