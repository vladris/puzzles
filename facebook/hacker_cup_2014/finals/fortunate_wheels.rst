Fortunate Wheels
================

Kit is competing on the popular game show, Fortunate Wheels. On this show,
there is a secret word **S** consisting only of uppercase letters, known
only to the host. Contestants can pay points to buy sequences of letters in
hopes of matching part of S and earning more points! This show is clearly a
scam, as the probability of earning more points than are spent is extremely low.
Fortunately, Kit has come prepared -- he knows the secret word! Even so, getting
as many points as possible will not be easy.

There are **N** *basic* deals which contestants can take. The i\ :sup:`th` deal
costs A\ :sub:`i` points, and allows the contestant to purchase any sequence
of B\ :sub:`i` letters. Furthermore, deals can be combined to purchase longer
sequences! Combining a deal with cost C\ :sub:`1` and length L\ :sub:`1`
with another deal (potentially the same one) with cost C\ :sub:`2` and length
L\ :sub:`2` creates a new deal with cost C\ :sub:`1` + C\ :sub:`2` + W and
length L\ :sub:`1` + L\ :sub:`2` (as long as L\ :sub:`1` + L\ :sub:`2` <
**|S|**), which can in turn be used to create even bigger deals. For example, if
W = 0, then a basic deal with cost and length equal to 1 could be combined with
itself repeatedly to yield a new deal with both cost and length equal to any
positive integer up to (but not including) **|S|**.

Once Kit purchases a sequence of letters using one (potentially non-basic) deal,
it will be matched against the secret word -- twice! The host will spin the
First Fortunate Wheel to select the starting index in S for the first matching,
which is chosen at uniform random such that the sequence will fit entirely
within **S**. Then, the host will spin the Second Fortunate Wheel to select the
starting index for the second matching, which is chosen at uniform random such
that the sequence will fit entirely within S and such that the value given by
the First Fortunate Wheel will not be repeated. For example, if the purchased
sequence consists of a single letter, the First Fortunate Wheel might yield any
of the indices in **S** with probability (1 / **|S|**) each, and then the Second
Fortunate Wheel might yield any of the remaining indices with probability
(1 / (**|S|**-1)) each. On the other hand, if the sequence has length
**|S|** − 1, then the First Wheel can yield either 0 or 1, and the Second Wheel
must yield the other. If, for both generated indices, the sequence miraculously
happens to be equal to the substring of **S** of the same length starting at
that index, then Kit will earn back Y(**|S| - |X − ℓ|**)\ :sup:`2` + Z points,
where **ℓ** is the length of the sequence. If even one letter is off in either
matching, however, Kit will earn no points at all!

Kit is carefully considering his first turn of the game. He obviously wants to
maximize the number of points he'll gain, but worries that choosing the very
best move might be suspicious. As such, he'd like to find the expected point
values of the M best distinct moves before making his decision. Two moves are
distinct iff they involve purchasing different sequences of letters - the deals
used are ignored. Note that moves can have negative expected point values, due
to the costs of deals.

Input
-----

Input begins with an integer **T**, the number of test cases. Each test case
begins with a line containing six integers, **N, M, W, X, Y, Z**. The next line
contains the string **S**. The next **N** lines each contain two integers,
A\ :sub:`i` and B\ :sub:`i`.

Output
------

For each test case *i*, output "Case #i: " followed by a space-separated list of
real numbers, the **M** largest expected point values which can be earned, in
order. Round these values off to 3 decimal places.

Constraints
-----------

1 ≤ **T** ≤ 20

2 ≤ **|S|** ≤ 105

1 ≤ **N** ≤ 20

1 ≤ A\ :sub:`i` ≤ 104

1 ≤ B\ :sub:`i` < **|S|**

0 ≤ **W** ≤ 104

1 ≤ **X** < **|S|**

0 ≤ **Y** ≤ 100

0 ≤ **Z** ≤ 100

1 ≤ **M** ≤ 20

Explanation of Sample
---------------------

In the first test case, Kit’s best move is to use the basic deal, costing 2
points, to purchase the sequence "Z". No matter what pair of indices the two
Fortunate Wheels yield, this sequence will match and earn Kit
5(2 - |1 - 1|)\ :sup:`2` + 6 = 26 points. Any other sequence shorter than
**|S|** cannot match at even a single index, so Kit’s second- and third-best
moves consist of using the basic deal to purchase any other single-letter
sequence, and simply losing the 2 points.

In the second test case, Kit’s best move consists of combining the third
basic deal with itself to yield a deal with cost 5 and length 4, and then
purchasing the sequence "OXEN". His three next-best moves, which are the only
other moves which get him a positive expected point value, involve using the
third basic deal to purchase the sequences "OX", "XE", and "EN".

Example input
-------------

::

    5
    1 3 0 1 5 6
    ZZ
    2 1
    3 4 1 4 3 2
    FOXENINBOXEN
    5 2
    1000 11
    2 2
    1 5 0 1 1 1
    AABB
    2 1
    1 5 0 1 10 1
    AAABBB
    2 1
    1 5 0 1 10 100
    AAAABBBB
    2 1

Example output
--------------

::

    Case #1: 24.000 -2.000 -2.000
    Case #2: 7.056 3.491 3.491 3.491
    Case #3: 0.833 0.833 -2.000 -2.000 -2.000
    Case #4: 70.200 70.200 21.100 21.100 -2.000
    Case #5: 156.571 156.571 80.286 80.286 24.667

`View online <https://www.facebook.com/hackercup/problems.php?pid=1418569468390467&round=180228228840273>`_.
