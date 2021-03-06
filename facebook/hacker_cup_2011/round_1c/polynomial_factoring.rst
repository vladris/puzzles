Polynomial Factoring
====================

A polynomial in x of degree **D** can be written as:

a\ :sub:`D`\ x\ :sup:`D` + a\ :sub:`D-1`\ x\ :sup:`D-1` + ... + a\ :sub:`1`\
x\ :sup:`1` + a\ :sub:`0`

In some cases, a polynomial of degree D can also be written as the product of
two polynomials of degrees D\ :sub:`1` and D\ :sub:`2`, where D = D\ :sub:`1`
+ D\ :sub:`2`. For instance,

4 x\ :sup:`2` + 11 x\ :sup:`1` + 6 = (4 x\ :sup:`1` + 3) * (1 x\ :sup:`1` + 2)

In this problem, you will be given two polynomials, denoted **F** and **G**.
Your task is to find a polynomial **H** such that **G** * **H** = **F**, and
each ai is an integer.

Input
-----

You should first read an integer **N** ≤ 60, the number of test cases. Each
test case will start by describing **F** and then describe **G**. Each
polynomial will start with its degree 0 ≤ D ≤ 20, which will be followed by
D+1 integers, denoting a\ :sub:`0`, a\ :sub:`1`, ... , a\ :sub:`D`, where
-10000 ≤ a\ :sub:`i` ≤ 10000. Each polynomial will have a non-zero
coefficient for it's highest order term.

Output
------

For each test case, output a single line describing **H**. If **H** has degree
D\ :sub:`H`, you should output a line containing D\ :sub:`H` + 1 integers,
starting with a\ :sub:`0` for **H**. If no **H** exists such that
**G** * **H** = **F**, you should output "no solution".

Example input
-------------

::

    5
    2 6 11 4
    1 3 4
    2 1 2 1
    1 1 1
    2 1 0 -1
    1 1 1
    1 1 1
    2 1 2 1
    5 1 1 1 1 1 1
    3 1 1 1 1

Example output
--------------

::

    Case #1: 2 1
    Case #2: 1 1
    Case #3: 1 -1
    Case #4: no solution
    Case #5: no solution

`View online <https://www.facebook.com/hackercup/problems.php?pid=157714037613443&round=173585106010813>`_.
