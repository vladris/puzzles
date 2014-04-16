Pizza Baking
============

Tony plans to open a pizzeria. After researching the pizza market for a long
time, he has come up with a prediction for the number of orders that he is
going to receive. Tony will keep his pizzeria open for **K** hours a day. And
he knows that he is going to get orders for **N** pizzas. Also pizza eaters are
very fussy, so the i\ :sup:`th` pizza must be inserted into an oven at
exactly the beginning of the S\ :sub:`i`\ :sup:`th` hour, and taken out of
the oven at exactly the end of the E\ :sub:`i`\ :sup:`th` hour.

For this purpose Tony needs to buy some ovens to be able to bake all the
ordered pizzas. Each oven is quite large, and can hold several pizzas at the
same time. However, due to voltage fluctuations throughout the day, only a
certain number of pizzas can be baked simultaneously in each oven at any point
of time. Tony has calculated the value C\ :sub:`i`, for 0 ≤ **i** < **K**,
denoting the number of pizzas that can be baked together in an oven during the
i\ :sup:`th` hour. A pizza that has been entered in an oven cannot be taken
out of the oven until it has completed its scheduled baking period.

High quality pizza ovens are very costly. Help Tony find out the minimum number
of ovens he must buy to complete all orders, and then find an assignment of
pizzas to ovens, satisfying all the constraints above. If there are multiple
assignments involving the same minimum number of ovens, print the smallest
possible assignment according to the ordering defined below.

Here's how you compare two assignments. If **X** is an assignment of pizzas to
ovens, let **X( i )** denote the set of 0-based pizza indices assigned to oven
**i** (oven indices are also 0-based).

If **S** and **T** are two sets of pizza indices, we say that **S** < **T**, if
and only if there exists some index **k**, such that:

* for 0 ≤ **i** < **k**, pizza **#i** either appears both in **S** and **T**,
  or is missing from both **S** and **T**, and,
* pizza **#k** is present in **S**, but missing in **T**

Example: {0, 2, 6} < {0, 3, 4} and {0, 1, 2, 3} < {0, 1, 2}

If **X** and **Y** are two pizza assignments, we say that **X** < **Y**, if and
only if there exists some **k**, such that:

* for 0 ≤ **i** < **k**, **X( i )** is identical to **Y( i )**, and,
* **X( k )** < **Y( k )**, as per the set ordering defined above.

Example:

**X** = [ **X** (0) = {0, 3, 6}, **X** (1) = {1, 4, 5}, **X** (2) = {2, 7} ]

**Y** = [ **Y** (0) = {0, 3, 6}, **Y** (1) = {1, 4}, **Y** (2) = {2, 5, 7} ]

Then **X** < **Y**, because **X** (0) = **Y** (0) and **X** (1) < **Y** (1).

Input
-----

The first line of the input consists of a single integer **T**, the number of
test cases.

Each test case starts with a line containing the integer **K**, the number of
hours the pizzeria will be open.

The next line of each test case contains **K** integers, C\ :sub:`0`, 
C\ :sub:`1`, ..., C\ :sub:`K-1`, where C\ :sub:`i` is the maximum number of
pizzas that can be inside any single oven in the ith hour.

The next line of each test case contains the integer **N**, the number of pizza
orders.

The next **N** lines of each test case contain a pair of integers,
S\ :sub:`i` and E\ :sub:`i`, the start and end times for baking the
i\ :sup:`th` pizza.

Output
------

For each test case **i** numbered from 1 to **T**, output "Case #i: ", followed
by **N** space separated integers. The jth integer must denote the 0-based oven
index that the j\ :sup:`th` pizza is assigned to.

Constraints
-----------

1 ≤ **T** ≤ 20

1 ≤ **K** ≤ 24

1 ≤ C\ :sub:`i` ≤ 100

1 ≤ **N** ≤ 1000

0 ≤ S\ :sub:`i` ≤ E\ :sub:`i` < **K**

Example input
-------------

::

    5
    2
    2 2
    3
    0 0
    1 1
    0 1
    4
    1 1 1 1
    7
    0 0
    0 1
    0 2
    0 3
    1 3
    2 3
    3 3
    3
    1 2 1
    4
    1 1
    0 1
    1 2
    0 2
    4
    2 2 2 2
    6
    0 1
    0 1
    1 2
    1 2
    2 3
    2 3
    5
    1 2 2 3 3
    12
    1 4
    2 3
    0 2
    2 4
    1 1
    3 4
    1 3
    0 1
    3 3
    2 4
    0 3
    4 4

Example output
--------------

::

    Case #1: 0 0 0
    Case #2: 0 1 2 3 0 1 2
    Case #3: 0 1 1 0
    Case #4: 0 0 1 1 0 0
    Case #5: 0 0 1 1 0 0 2 2 1 2 3 0

`View online <https://www.facebook.com/hackercup/problems.php?pid=1392143854367184&round=1433361756892155>`_.
