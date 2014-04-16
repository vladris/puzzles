Intervals of Love
=================

Do you remember helping Prince Z.A.Y. rescue the princess of the kingdom of
Hackadia from an evil dragon in Round 2? Well, as it so often happens, Z.A.Y.
has fallen in love with his dearest princess. However, the princess has given
Z.A.Y. a puzzle to solve to ensure that the one she marries is both brave and
clever.

The princess gives Z.A.Y a 0-indexed array of **N** integers, and she asks him a
series of questions. In each question, she provides an inclusive interval to the
prince, and asks him how many subarrays in that interval are slowly increasing.

A subarray is defined as a contiguous set of integers in the given array. A
subarray is slowly increasing iff each integer in the subarray after the first
is exactly 1 more than the previous integer. For example, **[1, 2, 3]**,
**[5]**, and **[10, 11, 12]** are slowly increasing, but **[7, 9]**,
**[13, 12, 11]**, and **[1, 1, 2, 2]** are not.

Easy problem, right? Yup, so the princess is going to make it more challenging
since she knows the prince is seeking help from the best Hackers from the world.
Sometimes, instead of asking a question, the princess will change an integer in
the array.

Still an easy problem, right? Probably, but the princess isn't going to make it
any harder (the prince *did* rescue her from a dragon, and could probably use a
break).

Input
-----

The first line consists of a single integer **T**, the number of test cases.
Each test case starts with a line containing an integer **N**, the length of the
array. Then 1 line follows with **N** integers X\ :sub:`i` representing the
elements of the array. Then 1 line follows with an integer **M**, the number of
actions the princess takes (questions and updates). Then **M** lines follow,
each with 3 integers. The first integer, **op**, represents the action the
princess takes. If **op** is 0, then 2 integers **P** and **K** follow, meaning
that the princess will change the **Pth** element of the array to **K**. If
**op** is 1, then 2 integers **L** and **R** follow, meaning that the princess
will ask how many slowly increasing subarrays there are between **L** and **R**
(inclusive).

Output
------

For each test case *i*, output "Case #i: " followed by a single integer, the
sum of the answers to the princess's questions. Since this number might be
large, output it modulo 1,000,000,007.

Explanation of Sample
---------------------

In the first sample case, the answer to the first question is 6 (the slowly
increasing subarrays are [4], [5], [6], [4, 5], [5, 6], [4, 5, 6]), and the
answer to the second question is 12. So the sum is 18.

In the second sample case, the answers are 3, 4, and 6 respectively, so the
sum is 13.

Constraints
-----------

1 ≤ **T** ≤ 20

1 ≤ **N** ≤ 10\ :sup:`6`

1 ≤ **M** ≤ 10\ :sup:`6`

1 ≤ **Xi**, **K** ≤ 10\ :sup:`9`

0 ≤ **P** < **N**

0 ≤ **op** ≤ 1

0 ≤ **L** ≤ **R** < N

Example input
-------------

::

    5
    8
    1 3 4 5 6 10 11 12
    2
    1 2 4
    1 2 7
    3
    1 1 1
    5
    1 0 2
    0 1 2
    1 0 2
    0 2 3
    1 0 2
    10
    4 5 1 3 8 1 5 2 4 1
    10
    1 0 3
    0 0 3
    0 0 2
    1 4 8
    1 8 8
    1 0 2
    0 0 3
    0 3 7
    0 8 6
    0 8 6
    10
    1 10 6 1 9 5 1 3 3 3
    10
    1 6 8
    1 6 9
    1 0 8
    0 0 3
    0 0 3
    0 4 8
    0 1 1
    0 0 1
    0 6 6
    0 0 1
    10
    9 1 3 1 5 5 5 1 1 2
    10
    1 5 8
    0 0 3
    1 0 2
    0 0 9
    0 3 4
    1 0 2
    0 5 1
    0 3 5
    0 0 7
    1 5 7

Example output
--------------

::

    Case #1: 18
    Case #2: 13
    Case #3: 14
    Case #4: 16
    Case #5: 13

`View online <https://www.facebook.com/hackercup/problems.php?pid=291408124369300&round=180228228840273>`_.
