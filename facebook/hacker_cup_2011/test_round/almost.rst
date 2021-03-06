Almost
======

For two integers **a** and **c**, we define **a** and a third integer **b** to
be almost factors of **c** by choosing the minimal **b** that minimizes
\| **ab** - **c** \|. Your task will be to determine **b** given **a** and **c**.

Input
-----

Your input file will consist of a single integer **N**, the number of test
cases in the file, followed by **N** pairs of integers **a** and **c**. All
tokens in the input will be separated by some whitespace.

Output
------

Your output should consist of **N** newline-separated integers, each one
representing **b** for the corresponding pair (**a**, **c**) in the input.

Constraints
-----------

5 ≤ **N** ≤ 20

1 ≤ **a**, **c** ≤ 1010

Example input
-------------

::

    5
    18 24
    77 176
    34 144
    24 426
    273 628

Example output
--------------

::

    Case #1: 1
    Case #2: 2
    Case #3: 4
    Case #4: 18
    Case #5: 2

`View online <https://www.facebook.com/hackercup/problems.php?pid=181903565165188&round=103456299728530>`_.
