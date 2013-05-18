Scott's New Trick
=================

Little Scott recently learned how to perform arithmetic operations modulo some
prime number **P**. As a training set he picked two sequences **a** of length
**N** and **b** of length **M**, generated in the following way:

a\ :sub:`1`\ =A1
a\ :sub:`2`\ =A2
a\ :sub:`i`\ =(a\ :sub:`i-2` * A3 + a\ :sub:`i-1` * A4 + A5) mod P, for i=3...
**N**
b\ :sub:`1`\ =B1
b\ :sub:`2`\ =B2
b\ :sub:`j`\ =(b\ :sub:`j-2` * B3 + b\ :sub:`j-1` * B4 + B5) mod P, for j=3...
**M**

Now he wants to find the number of pairs (i, j), where 1 ≤ i ≤ **N** and 1 ≤ j
≤ **M**, such that (a\ :sub:`i` * b\ :sub:`j`) mod **P** < **L**, for given
number **L**. He asked you to do the same to help him check his answers.

Input
-----

The first line of input file consists of a single number **T**, the number of
test cases. Each test consists of three lines. The first line of a test case
contains two integers: prime number **P** and positive integer **L**. The
second line consists of six non-negative integers **N**, **A1**, **A2**,
**A3**, **A4**, **A5**. Likewise, the third line contains six non-negative
integers **M**, **B1**, **B2**, **B3**, **B4**, **B5**.

Output
------

Output **T** lines, with the answer to each test case on a single line.

Constraints
-----------

**T** = 20

2 ≤ **P** < 250,000

**P** is prime

1 ≤ **L** ≤ **P**

2 ≤ **N**, **M** ≤ 10,000,000

0 ≤ **A1**, **A2**, **A3**, **A4**, **A5**, **B1**, **B2**, **B3**,
**B4**, **B5** < P

Example input
-------------

::

    5
    3 1
    4 0 2 2 2 2
    2 1 2 1 0 0
    3 1
    5 2 0 0 1 1
    5 1 1 2 0 0
    3 3
    5 0 0 1 2 2
    3 2 1 1 1 1
    5 1
    5 2 0 4 0 4
    3 2 1 2 4 4
    5 4
    2 2 1 3 1 4
    5 1 0 2 3 3

Example output
--------------

::

    Case #1: 6
    Case #2: 10
    Case #3: 15
    Case #4: 3
    Case #5: 9

`View online <https://www.facebook.com/hackercup/problems.php?pid=134500253280699&round=178767375498716>`_.
