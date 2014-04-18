Secret Santa
============

There are **K** families living in Christmasville. During Christmas they have
this tradition, where each person secretly gets a gift for some other person.
The assignment of who gives gift to whom is generally done by a lottery, but
this time we are writing a program to do it.

The assignment should have the following properties:

* Each person should give exactly one gift.
* Each person should receive exactly one gift.
* A person should not give a gift to someone within the same family.

Find out how many possible assignments are there, that satisfy above
constraints. Two assignments are considered different, if there exists some
person, who gives gifts to different people in the two assignments. Since this
number may be very large, output this number modulo 1,000,000,007

Input
-----

The first line of the input consists of a single integer **T**, the number of
test cases.

Each test case starts with a line containing the integer **K**, the number of
families.

The next line of each test case contains **K** integers, n\ :sub:`1`,
n\ :sub:`2`, ..., n\ :sub:`K`, where n\ :sub:`i` is the number of people in
the i\ :sup:`th` family.

Output
------

For each test case **i** numbered from 1 to **T**, output "Case #i: ", followed
by the number of valid assignments, modulo 1,000,000,007

Constraints
-----------

1 ≤ **T** ≤ 20

2 ≤ **K** ≤ 100

1 ≤ n\ :sub:`i` ≤ 4

1 ≤ n\ :sub:`1` + n\ :sub:`2` + ... + n\ :sub:`K` ≤ 100

Example input
-------------

::

    5
    2
    1 1
    3
    1 1 1
    2
    2 2
    3
    2 2 2
    4
    1 2 3 4

Example output
--------------

::

    Case #1: 1
    Case #2: 2
    Case #3: 4
    Case #4: 80
    Case #5: 97344

`View online <https://www.facebook.com/hackercup/problems.php?pid=1427296790834577&round=1433361756892155>`_.
