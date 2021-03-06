Trapezoids
==========

Consider two horizontal lines and a set of **N** trapezoids. A trapezoid
**T[i]** between these lines has two vertices situated on the upper line and
the other two vertices on the lower line. We will denote by **a[i]**, **b[i]**,
**c[i]** and **d[i]** the upper left, upper right, lower left and respectively
lower right vertices of the trapezoid **T[i]**. Assume that no two trapezoids
share a common vertex (meaning that all **a[i]** and **b[i]** coordinates on
the upper line are different, and the same holds for the bottom line and
coordinates **c[i]** and **d[i]**). A trapezoid set is called **disconnected**
if one can separate the trapezoids in two or more groups such that no two
trapezoids from different groups intersect. Determine the smallest number of
trapezoids to remove, such that the remaining trapezoids form a disconnected
set. If the solution does not exist, output **-1**.

Input
-----

The first line of the input file contains an integer **T**, and this is
followed by **T** test cases. Each test case is given in the compressed format.

The first line of each test case contains the number of trapezoids **N**, an
integer **K**, and integer parameters **X, A, B, M, p, q**. In the next **K**
lines are given integer numbers **aa[i], bb[i], cc[i], dd[i]**. The following
code is used for generating the next random number using linear congruential
generator with the starting value **X** and parameters **A, B** and modulo
**M**:

::

    long long prior = X;
    long long next() {
      prior = (A * prior + B) % M;
      return prior;
    }

The following code is used for extending the auxiliary sequences **aa, bb, cc**
and **dd**:

::

    for (int i = K; i < N; i++) {
        aa [i] = aa [i - K] + next() % (2 * p) - p;
        bb [i] = aa [i] + 1 + next() % (2 * (bb [i % K] - aa [i % K]));
        cc [i] = cc [i - K] + next() % (2 * q) - q;
        dd [i] = cc [i] + 1 + next() % (2 * (dd [i % K] - cc [i % K]));
    }

The final coordinates of the trapezoids are given by:

::

    for (int i = 0; i < N; i++) {
        a [i] = aa [i] * 1000000 + i;
        b [i] = bb [i] * 1000000 + i;
        c [i] = cc [i] * 1000000 + i;
        d [i] = dd [i] * 1000000 + i;
    }

Note that above code generates trapezoids that satisfy all conditions of the
problem, and '%' denotes the remainder of division.

Output
------

For each of the test cases numbered in order from **1** to **T**, output "Case
#i: " followed by a single integer, the minimum number of trapezoids that need
to be removed such that the remaining trapezoids form a disconnected set.

Constraints
-----------

1 ≤ **T** ≤ 20

1 ≤ **N** ≤ 300 000

1 ≤ **K** ≤ **N**

0 ≤ **X, A, B** ≤ 2 000 000 000

-2 000 000 000 ≤ **aa[i], bb[i], cc[i], dd[i]** ≤ 2 000 000 000

1 ≤ **p, q, M** ≤ 2 000 000 000

Examples
--------

In the first example, one can remove trapezoids 5 and 6 leaving two disconnected
sets with trapezoids (1, 2, 3, 4) and (7, 8).

In the second example, the coordinates of ten trapezoids are

::

    1000000 4000000 3000000 5000000
    7000001 8000001 2000001 6000001
    2000002 7000002 2000002 5000002
    5000003 7000003 2000003 6000003
    4 6000004 2000004 3000004
    4000005 5000005 3000005 8000005
    -999994 6 6 2000006
    4000007 6000007 1000007 7000007
    -999992 8 -999992 2000008
    5000009 6000009 9 7000009

Example input
-------------

::

    5

    8 8 1 1 1 1 1 1
    1 3 1 3
    2 5 6 10
    4 8 5 8
    6 9 2 4
    7 11 11 13
    10 13 7 9
    12 16 14 15
    14 15 12 16

    10 2 2 1 1 7 2 2
    1 4 3 5
    7 8 2 6

    100000 2 1 1 1 2 1 1
    -2 -1 -1000001 -1000000
    -1000001 -1000000 -2 -1

    200 3 5 1 2 1117 11 13
    1 10 1 10
    2 11 2 11
    3 12 3 12

    10000 1 0 0 1 2 1 1
    1 10000 1 100000

Example output
--------------

::

    Case #1: 2
    Case #2: 6
    Case #3: 50002
    Case #4: 61
    Case #5: -1

`View online <https://www.facebook.com/hackercup/problems.php?pid=182208915220500&round=222291111185610>`_.
