N-Factorful
===========

A number is called **n**\ -factorful if it has exactly **n** distinct prime
factors. Given positive integers **a**, **b**, and **n**, your task is to
find the number of integers between **a** and **b**, inclusive, that are
**n**\ -factorful. We consider 1 to be 0-factorful.

Input
-----

Your input will consist of a single integer **T** followed by a newline and
**T** test cases. Each test cases consists of a single line containing integers
**a**, **b**, and **n** as described above.

Output
------

Output for each test case one line containing the number of **n**\ -factorful
integers in [**a**, **b**].

Constraints
-----------

**T** = 20

1 ≤ **a** ≤ **b** ≤ 107

0 ≤ **n** ≤ 10

Example input
-------------

::

    5
    1 3 1
    1 10 2
    1 10 3
    1 100 3
    1 1000 0

Example output
--------------

::

    Case #1: 2
    Case #2: 2
    Case #3: 0
    Case #4: 8
    Case #5: 1

`View online <https://www.facebook.com/hackercup/problems.php?pid=172875359424547&round=173585106010813>`_.
