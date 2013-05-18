Diversity Number
================

Let's call a sequence of integers a\ :sub:`1`, a\ :sub:`2`, ..., a\ :sub:`N`
*almost monotonic* if first K elements are non-decreasing sequence and last
N-K+1 elements are non-increasing sequence: a\ :sub:`1`\ ≤a\ :sub:`2`\
≤...≤a\ :sub:`K` and a\ :sub:`K`\ ≥a\ :sub:`K+1`\ ≥...≥a\ :sub:`N`.

The diversity number of a sequence a\ :sub:`1`, a\ :sub:`2`, ..., a\ :sub:`N`
is the number of possible sequences b\ :sub:`1`, b\ :sub:`2`,..., b\ :sub:`N`
for which 0≤b\ :sub:`i`\ <a\ :sub:`i` and all of the numbers b\ :sub:`1`,
b\ :sub:`2`,..., b\ :sub:`N` are different. The diversity number of an empty
sequence is 1.

You need to find the sum of the diversity numbers of all almost monotonic
subsequences of a sequence. Since this number can be very large, find it
modulo 1,000,000,007. A subsequence is a sequence that can be obtained from
another sequence by deleting some elements without changing the order of the
remaining elements. Two sequences are considered different if their lengths
differ or there is at least one position at which they differ.

Input
-----

The first line of the input file consists of a single number **T**, the number
of test cases. Each test case consists of a number **M**, the number of
elements in a sequence, followed by **M** numbers **n**, elements of some
sequence (note that this sequence is not necessarily *almost monotonic*). All
tokens are whitespace-separated

Constraints
-----------

**T** = 20

1 ≤ **M**, **n** ≤ 100

Output
------

Output **T** lines, with the answer to each test case on a single line.

Example input
-------------

::

    5
    1
    1
    2
    2 1
    3
    1 3 2
    4
    1 3 1 2
    4
    2 3 4 3

Example output
--------------

::

    Case #1: 2
    Case #2: 5
    Case #3: 15
    Case #4: 17
    Case #5: 80

`View online <https://www.facebook.com/hackercup/problems.php?pid=127561170642475&round=123802894356576>`_.
