Archiver
========

You are writing a new revolutionary archiver. The archive is essentially a pair
of non-decreasing sequences of integers of equal length **K**:
0≤x\ :sub:`1`\ ≤...≤x\ :sub:`k` and 0≤y\ :sub:`1`\ ≤...≤y\ :sub:`k`.

The decompression algorithm proceeds as follows:

1. Sequence (0,0), (x\ :sub:`1`, y\ :sub:`1`), ... (x\ :sub:`k`, y\ :sub:`k`), 
   (x\ :sub:`k`, 0), (0, 0) defines a polygon **P**
2. Starting from the point **(0,0)**, increase either **x** or **y** coordinate
   by 1 without moving outside of **P**. If both moves are available, you
   should increase **y**. After each step write **0** to output if incremented
   **x** or **1** otherwise.
3. Repeat step 2 until you end up in point (x\ :sub:`k`, y\ :sub:`k`).

Example: decompression of sequence **(3,4), (7,6), (7,8)** will produce string
**010101100100111**.

Your task is to write a compression rate calculator, that is given binary
string s find the smallest value of **K** for which there exists archive that
decompresses to s.

Input
-----

The first line contains a single integer **T**, **T** ≤ 20. T test cases
follow, where each test case consists of one binary string with length
**≤ 1000000**.

Output
------

Output a single line containing the smallest possible **K**.

Example input
-------------

::

    5
    001
    10011
    0010101
    1110
    0110

Example output
--------------

::

    Case #1: 1
    Case #2: 3
    Case #3: 1
    Case #4: 2
    Case #5: 2

`View online <https://www.facebook.com/hackercup/problems.php?pid=553275214705025&round=430084003727512>`_.
