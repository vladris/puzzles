Turn on the Lights
==================

A simple game consists of a grid of **R**\ x\ **C** buttons. Each button will
be either lighted, or unlighted. Whenever you push a button, the state of that
button, and its (up to) four neighbors will toggle -- lighted buttons will
become unlighted and unlighted buttons will become lighted. Note that the
neighbors do not 'wrap' and thus a corner button has only two neighbors, while
an edge buttons has three.

In this problem you will be given an initial configuration of the buttons. Your
task is to push the right buttons so that, when you are done, all of the lights
are turned on. If there are multiple ways to do this, you should determine the
minimum number of buttons pushes that it can be done in.

Input
-----

You will first read an integer **N** the number of test cases. For each test
case, you will read two integers **R** and **C**. This will be followed by
**R** whitespace-separated tokens, each containing **C** characters. A 'X'
indicates a lighted button, while a '.' indicates an unlighted button.

Constraints
-----------

**N** = 20

1 ≤ **R**, **C** ≤ 18

Output
------

For each test case you should output the minimum number of button presses
required to turn on all the lights. If there is no way to do this, you should
output -1.

Example input
-------------

::

    5
    5 6
    XXXXXX
    XXX.X.
    XXXXXX
    X.XXXX
    XXXXX.
    1 13
    ..XXXXXXX.X..
    11 6
    XXXXXX
    XXXXXX
    XXXXXX
    XXXXXX
    XXXXXX
    XXXXXX
    XXXXXX
    .X.XXX
    XXXX.X
    XXXXXX
    XXX.XX
    10 13
    ..XX...X.X.X.
    XX..X..X.....
    .X...........
    X........X...
    .....XX..X.X.
    .X..XX.......
    .X.....X.X...
    .X....X......
    ......XX...X.
    ..X....X.....
    9 3
    ...
    ...
    ...
    ...
    ...
    ..X
    ...
    ...
    ...

Example output
--------------

::

    Case #1: 14
    Case #2: 7
    Case #3: 27
    Case #4: 65
    Case #5: 11

`View online <https://www.facebook.com/hackercup/problems.php?pid=158877957461506&round=123802894356576>`_.
