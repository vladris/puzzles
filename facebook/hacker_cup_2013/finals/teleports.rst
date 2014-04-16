Teleports
=========

Your house has **2 ≤ N ≤ 500,000** distinct rooms. None of the rooms have
doors, but every room has a one way teleport which takes you to a different
room. The same teleport will always go to the same room. You want to make sure
that every room can be reached from every room, via a series of teleports. To
do this, you are allowed to change the destination of some (or all) of the
teleports.

What is the sum of the minimum number of teleports you have to change to
achieve this, over all possible different starting configurations? Two starting
configurations are different if for some room, the outgoing teleport goes to
different rooms in the two configurations.

Input
-----

The first line contains a single integer **T**, **T** ≤ 20. **T** test cases
follow, where each test case consists of one integer: **N**

Output
------

Output one single line with the sum of the minimum number of teleports you have
to change over all possible different starting configurations. Since this
number might be very big, output it modulo **1,000,000,007**

Example input
-------------

::

    5
    2
    3
    5
    10
    20

Example output
--------------

::

    Case #1: 0
    Case #2: 6
    Case #3: 1720
    Case #4: 435035973
    Case #5: 93930085

`View online <https://www.facebook.com/hackercup/problems.php?pid=157234401098548&round=430084003727512>`_.
