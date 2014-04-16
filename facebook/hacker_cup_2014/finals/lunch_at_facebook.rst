Lunch at Facebook
=================

What's the best thing about working at Facebook? It's hard to say, but the free
food doesn't hurt. Every day there are long lines for food, and sometimes
guests visit the campus, as hungry as everybody else. It pays to be a good host,
so sometimes we'll let guests cut ahead in the line. But obviously nobody wants
to miss out on delicious Facebook food.

Every day, **N** Facebook employees are lined up for lunch, and every day **M**
visitors come to the campus looking for food. Each person has an appetite
A\ :sub:`i`, which is a positive integer. Curiously, no two people have the
same appetite.

If people with large appetites eat first, there's a concern that the food might
run out before the people at the back get to eat, so it's ideal to have people
with smaller appetites further ahead in the line. With this in mind, we'd like
to squeeze all of the guests into the lunch line as efficiently as possible.

We define the *unsuitableness* of a line as the number of pairs of people in
the line, P\ :sub:`i` and P\ :sub: `j`, such that P\ :sub:`i` is ahead
of P\ :sub:`j` in the line, and P\ :sub:`i` has a larger appetite than
P\ :sub:`j`. Your task is to find a way to get all the visitors into the
lunch line such that the unsuitableness of the resulting line is minimized. The
employees that are standing in line won't change order, but you can put guests
in any place you want.

Input
-----

The first line contains an integer **T**, the number of test cases.

Each test case has three lines:

A line with **N** and **M**.

A line with **N** integers, the appetites of the employees in order, beginning
with the first employee.

A line with **M** integers, the appetites of the visitors.

Output
------

For each test case *i*, output "Case #i: " followed by the minimum possible
unsuitableness of the resulting line.

Constraints
-----------

1 ≤ **T** ≤ 20
1 ≤ **N** ≤ 105
1 ≤ **M** ≤ 105
1 ≤ A\ :sub:`i` ≤ 109

Explanation of Sample
---------------------

For the first test case the optimal lunch line has the following appetites in
order: 1, 2, 3, 4

For the second test case the optimal lunch line is: 1, 2, 4, 7, 5, 3

Example input
-------------

::

    5
    2 2
    1 2
    3 4
    4 2
    1 7 5 3
    2 4
    10 5
    9 3 14 13 7 10 12 1 6 8
    2 15 5 4 11
    10 5
    7 9 3 14 10 4 5 1 13 6
    2 15 11 8 12
    10 5
    2 8 10 7 12 5 13 11 4 6
    3 9 14 15 1

Example output
--------------

::

    Case #1: 0
    Case #2: 4
    Case #3: 35
    Case #4: 33
    Case #5: 25

`View online <https://www.facebook.com/hackercup/problems.php?pid=582461561843577&round=180228228840273>`_.
