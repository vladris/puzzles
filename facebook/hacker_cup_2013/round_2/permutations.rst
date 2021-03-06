Permutations
============

In this problem you need to count number of possible permutations **p** of the
first **N** integers, given **N-1** constraints of the form **p**\ :sub:`i` 
< **p**\ :sub:`j`.

Input
-----

The first line contains an integer **T**, **T** ≤ 20, followed by **T** test
cases. Each test case begins with an integer **N**, **N** ≤ 1000, which is
the number of integers in the permutation. The next **N - 1** lines each
contain a single constraint in the following format: "**i sign j**", where 0
≤ **i, j** ≤ **N - 1** and sign is either "<" or ">", which denotes whether
the **i**-th element of the permutation should be less than or greater than the
**j**-th element.

It is guaranteed that it is not possible to partition indices into two disjoint
sets A and B such that there is no constraint involving elements from both A
and B.

Output
------

For each test case, output one single line with the number of permutations that
satisfy all the constraints, following the output format shown in the example.
The answer may be very large, so you should give the result modulo
**1000000007**.

Example input
-------------

::

    5
    2
    0 < 1
    3
    0 < 1
    2 > 1
    5
    0 < 2
    1 < 2
    2 < 3
    2 < 4
    4
    0 < 1
    0 < 2
    0 < 3
    6
    0 > 1
    1 > 2
    2 > 3
    3 > 4
    4 > 5

Example output
--------------

::

    Case #1: 1
    Case #2: 1
    Case #3: 4
    Case #4: 6
    Case #5: 1

`View online <https://www.facebook.com/hackercup/problems.php?pid=413074315443326&round=499927843385312>`_.
