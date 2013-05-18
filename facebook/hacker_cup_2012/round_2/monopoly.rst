Monopoly
========

In a certain business sector there are currently N small companies, each having
just a single employee. These employees are numbered 1 through N.

The business sector is about to be transformed into a monopoly. This will
happen through a series of mergers, until there is only one company. A single
merger involves two companies. In a merger, the president of one company
becomes the direct report of the president of the other company, preserving the
rest of the hierarchies of both companies.

You will be given the descriptions of all mergers. Depending on how they are
performed (which of the two presidents involved becomes the president of the
new company), the hierarchy can of the final company can take different
shapes. We want the hierarchy of the final company to be as shallow as
possible. The task is to find the smallest possible number of levels in the
final hierarchy.

There is also a limit D on the number of direct reports any employee can have.
Because of this limit, there may be only one way to accomplish a certain
merger, or it might even be impossible. However, there will always be some way
to accomplish all the mergers.

Input
-----

The first line contains the number of test cases T.

Each test case starts with a blank line. The next line contains two integers,
N and D.

Each of the following N-1 lines describes a single merger, with two integers
between 1 and N. These are the employees whose companies are merging. The two
employees will never already be part of the same company.

The mergers must be performed in the order in which they are given.

Constraints
-----------

5 ≤ T ≤ 20

2 ≤ N ≤ 30000

1 ≤ D ≤ 5000

The input test cases will be such that it is possible to accomplish all
mergers.

Output
------

For each of the test cases numbered in order from 1 to T, output "Case #i: "
followed by a single integer, the smallest number of levels in the final
hierarchy.

Examples
--------

In the first example, we have N=3 and D=2. The first merger happens between the
companies of employees 1 and 2. In the resulting company we can have employee 1
as the president with 2 as his report, or vice versa. Next this company merges
with the company of employee 3. If we have employee 3 become the president, the
hierarchy will be a chain 3-1-2 or 3-2-1. If 1 or 2 become the president, that
president will have the other two employees as direct reports. This last
hierarchy has two levels.

Example input
-------------

::

    5

    3 2
    1 2
    1 3

    3 1
    1 2
    1 3

    4 2
    4 2
    2 1
    3 2

    5 2
    5 2
    4 5
    2 1
    3 1

    6 3
    6 1
    4 2
    1 4
    5 6
    3 6

Example output
--------------

::

    Case #1: 2
    Case #2: 3
    Case #3: 3
    Case #4: 3
    Case #5: 4

`View online <https://www.facebook.com/hackercup/problems.php?pid=299871816717968&round=154897681286317>`_.
