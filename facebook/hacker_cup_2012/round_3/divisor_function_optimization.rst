Divisor Function Optimization
=============================

Let **d(N)** be the number of positive divisors of positive integer **N**.
Consider the infinite sequence **x(n) = d(n)a / nb, n = 1, 2, 3, …** where
**a** and **b** are fixed positive integers. It can be shown that this
sequence tends to zero. Hence it attains its maximum. Denote it by **p/q**
where **p** and **q** are co-prime positive integers. Your task is for given
**a** and **b** find **p** and **q** modulo **M = 10\ :sup:`9`+7**. But to
keep input and output small you will be given tuples **(b1; b2; a1; a2; c)**
and need to calculate the sum of **(p mod M)** for all pairs **(a; b)** such
that **b1 ≤ b ≤ b2**, **a1 ≤ a ≤ a2** and **a ≤ c*b**, and the same
sum for **q**-values.

Input
-----

The first line contains a positive integer **T**, the number of test cases.
**T** test cases follow. The only line of each test case contains five space
separated positive integers **b1**, **b2**, **a1**, **a2** and **c**.

Output
------

For each of the test cases numbered in order from **1** to **T**, output "Case
#i: " followed by a space separated pair of integers: the sum of **(p mod M)**
for all pairs **(a; b)** mentioned above and the sum of **(q mod M)** for all
such pairs. Note that you need to find the sum of residues not the residue of
sum (see testcase 3 as a reference).

Constraints
-----------

1 ≤ **T** ≤ 20

1 ≤ **b1** ≤ **b2** ≤ 10000

1 ≤ **a1** ≤ **a2** ≤ 250000

1 ≤ **c** ≤ 25

in each testcase the total number of pairs **(a; b)** for which the answer
should be calculated does not exceed 100000

Example input
-------------

::

    5
    1 1 1 3 10
    1 2 1 88 3
    1 10 1 50 5
    1 1 1 15 15
    30 33 1 29 25

Example output
--------------

::

    Case #1: 1540 37
    Case #2: 2377233 1491
    Case #3: 75232917907 54682660016
    Case #4: 5956707232 7441063226
    Case #5: 116 116

`View online <https://www.facebook.com/hackercup/problems.php?pid=249570461788103&round=222291111185610>`_.
