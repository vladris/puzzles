Double Squares
==============

A double-square number is an integer **X** which can be expressed as the sum of
two perfect squares. For example, 10 is a double-square because 10 = 3\
:sup:`2` + 1 :sup:`2`\. Your task in this problem is, given **X**, determine
the number of ways in which it can be written as the sum of two squares. For
example, 10 can only be written as 3\ :sup:`2` + 1\ :sup:`2` (we don't count
1\ :sup:`2` + 3\ :sup:`2` as being different). On the other hand, 25 can be
written as 5\ :sup:`2` + 0\ :sup:`2` or as 4\ :sup:`2` + 3\ :sup:`2`.

Input
-----

You should first read an integer **N**, the number of test cases. The next
**N** lines will contain **N** values of **X**.

Constraints
-----------

0 ≤ **X** ≤ 2147483647

1 ≤ **N** ≤ 100

Output
------

For each value of **X**, you should output the number of ways to write **X** as
the sum of two squares.

Example input
-------------

::

    5
    10
    25
    3
    0
    1

Example output
--------------

::

    Case #1: 1
    Case #2: 2
    Case #3: 0
    Case #4: 1
    Case #5: 1

`View online <https://www.facebook.com/hackercup/problems.php?pid=112921602098268&round=4>`_.
