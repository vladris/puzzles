Magic Pairs
===========

The princess of the kingdom of Hackadia has been kidnapped by an evil dragon. 
As always the prince Z.A.Y. is going to try to rescue her. The evil dragon is
keeping the princess prisoner in his deepest dungeon, and the prince has to
solve a puzzle to get her out safely.

There are two straight boards in front of the dungeon, both divided into a
large number of sections. Each section contains a sparkling gemstone. Each 
stone has a color. We will denote these colors with numbers.

Let's say these boards Board\ :sub:`1` and Board\ :sub:`2` contain **N** and
**M** sections respectively. 
Let's call a pair of integers **x**, **y** a magic pair if they have the
following properties:

1. 0 ≤ **x** < **N**
2. 0 ≤ **y** < **M**
3. The set of different colors in Board\ :sub:`1`\ [0...x] equals the set of different colors in Board\ :sub:`2`\ [0...y].

The prince has asked you to find out how many magic pairs exist for the given
two boards, so he can free the princess and become the hero. He will take all
the glory from this, so you will have to make do with points in this
competition as payment for your help.

Since the numbers **N** and **M** might be very large, the colors of the
gemstones will be supplied through a pseudo random generator. This works as
follows:

Board\ :sub:`1`\ [0] = **x1**

Board\ :sub:`2`\ [0] = **x2**

Board\ :sub:`1`\ [i] = (a1 * Board\ :sub:`1`\ [(i-1) % N] + b1 *
Board\ :sub:`2`\ [(i-1) % M] + c1) % r1, for 0 < i < N

Board\ :sub:`2`\ [i] = (a2 * Board\ :sub:`1`\ [(i-1) % N] + b2 * 
Board\ :sub:`2`\ [(i-1) % M] + c2) % r2, for 0 < i < M

Input
-----

The first line of the input consists of a single integer **T**, the number of
test cases. 

Each test case starts with a line containing the integers **N, M**

The second line of each test case contains five integers **x1, a1, b1, c1, r1**

The third line of each test case contains five integers **x2, a2, b2, c2, r2**

Output
------

For each test case i numbered from **1** to **T**, output "Case #i: ", followed
by the number of magic pairs for the two boards.

Constraints
-----------

1 ≤ **T** ≤ 20 

1 ≤ **N, M** ≤ 10^6

0 ≤ **x1, x2, a1, a2, b1, b2, c1, c2** ≤ 10^9

1 ≤ **r1, r2** ≤ 10^9 

Examples
--------

The first example produces the following boards:

Board\ :sub:`1` = [0, 3, 2, 0, 4, 2, 1, 3]

Board\ :sub:`2` = [0, 4, 2, 1, 4, 3]

There are 3 magic pairs:

pair(0, 0) ==> (0)

pair(6, 5) ==> (0, 1, 2, 3, 4)

pair(7, 5) ==> (0, 1, 2, 3, 4)

Example input
-------------

::

    5
    8 6
    0 0 1 3 5
    0 1 0 4 5
    5 5
    2 5 2 5 7
    2 9 3 2 7
    12 11
    2 5 2 5 7
    2 9 3 2 7
    10 10
    0 1 0 1 11
    0 0 1 1 11
    10 10
    0 1 0 1 11
    0 0 1 10 11

Example output
--------------

::

    Case #1: 3
    Case #2: 3
    Case #3: 6
    Case #4: 10
    Case #5: 1

`View online <https://www.facebook.com/hackercup/problems.php?pid=620734011349888&round=544142832342014>`_.
