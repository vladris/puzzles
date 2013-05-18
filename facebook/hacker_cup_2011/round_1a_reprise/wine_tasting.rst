Wine Tasting
============

A group of Facebook employees just had a very successful product launch. To
celebrate, they have decided to go wine tasting. At the vineyard, they decide
to play a game. One person is given some glasses of wine, each containing a
different wine. Every glass of wine is labelled to indicate the kind of wine
the glass contains. After tasting each of the wines, the labelled glasses are
removed and the same person is given glasses containing the same wines, but
unlabelled. The person then needs to determine which of the unlabelled glasses
contains which wine. Sadly, nobody in the group can tell wines apart, so they
just guess randomly. They will always guess a different type of wine for each
glass. If they get enough right, they win the game. You must find the number
of ways that the person can win, modulo 1051962371.

Input
-----

The first line of the input is the number of test cases, **N**. The next **N**
lines each contain a test case, which consists of two integers, **G** and
**C**, separated by a single space. **G** is the total number of glasses of
wine and **C** is the minimum number that the person must correctly identify to
win.

Constraints
-----------

**N** = 20

1 ≤ **G** ≤ 100

1 ≤ **C** ≤ **G**

Output
------

For each test case, output a line containing a single integer, the number of
ways that the person can win the game modulo 1051962371.

Example input
-------------

::

    5
    1 1
    4 2
    5 5
    13 10
    14 1

Example output
--------------

::

    Case #1: 1
    Case #2: 7
    Case #3: 1
    Case #4: 651
    Case #5: 405146859

`View online <https://www.facebook.com/hackercup/problems.php?pid=100623926681599&round=123802894356576>`_.
