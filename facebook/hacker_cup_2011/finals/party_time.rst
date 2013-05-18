Party Time
==========

You're throwing a party for your friends, but since your friends may not all
know each other, you're afraid a few of them may not enjoy your party. So to
avoid this situation, you decide that you'll also invite some friends of your
friends. But who should you invite to throw a great party?

Luckily, you are in possession of data about all the friendships of your
friends and their friends. In graph theory terminology, you have a subset **G**
of the social graph, whose vertices correspond to your friends and their
friends (excluding yourself), and edges in this graph denote mutual
friendships. Furthermore, you have managed to obtain exact estimates of how
much food each person in **G** will consume during the party if he were to be
invited.

You want to choose a set of guests from **G**. This set of guests should
include all your friends, and the subgraph of **G** formed by the guests must
be connected. You believe that this will ensure that all of your friends will
enjoy your party since any two of them will have something to talk about...

In order to save money, you want to pick the set of guests so that the total
amount of food needed is as small as possible. If there are several ways of
doing this, you prefer one with the fewest number of guests.

The people/vertices in your subset **G** of the social graph are numbered from
0 to **N** - 1. Also, for convenience your friends are numbered from 0 to **F**
- 1, where **F** is the number of your friends that you want to invite. You may
also assume that **G** is connected. Note again that you are not yourself
represented in **G**.

Input
-----

The first line of the input consists of a single number **T**, the number of
test cases. Each test case starts with a line containing three integers **N**,
the number of nodes in **G**, **F**, the number of friends, and **M**, the
number of edges in **G**. This is followed by **M** lines each containing two
integers. The **i**:sup:`th` of these lines will contain two distinct integers
**u** and **v** which indicates a mutual friendship between person **u** and
person **v**. After this follows a single line containing **N** space-separated
integers with the **i**:sup:`th` representing the amount of food consumed by
person **i**.

Output
------

Output **T** lines, with the answer to each test case on a single line by
itself. Each line should contain two numbers, the first being the minimum total
quantity of food consumed at a party satisfying the given criteria and the
second the minimum number of people you can have at such a party.

Constraints
-----------

**T** = 50

1 ≤ **F** ≤ 11

**F** ≤ **N** - 1

2 ≤ **N** ≤ 250

**N** - 1 ≤ **M** ≤ **N** * (**N** - 1) / 2

**G** is connected, and contains no self-loops or duplicate edges.

For each person, the amount of food consumed is an integer between 0 and 1000, both inclusive.

Example input
-------------

::

    5
    3 2 2
    0 2
    1 2
    1 2 3
    4 2 4
    0 2
    0 3
    1 2
    1 3
    0 0 1000 11
    8 3 13
    0 4
    0 5
    1 3
    1 4
    1 7
    2 7
    2 6
    3 4
    3 7
    3 5
    3 6
    4 5
    6 7
    4 10 14 100 99 24 25 50
    10 5 15
    0 8
    0 5
    1 5
    1 9
    1 8
    1 6
    2 9
    3 6
    3 5
    3 8
    4 8
    4 6
    4 5
    5 6
    6 7
    6 4 7 3 3 1 2 3 7 4
    11 7 12
    0 10
    1 8
    1 9
    2 8
    2 10
    3 8
    4 9
    5 9
    6 10
    6 7
    8 9
    8 10
    7 5 4 3 2 7 0 9 7 5 5

Example output
--------------

::

    Case #1: 6 3
    Case #2: 11 3
    Case #3: 177 5
    Case #4: 28 7
    Case #5: 45 10

`View online <https://www.facebook.com/hackercup/problems.php?pid=198773576808963&round=188859297819219>`_.
