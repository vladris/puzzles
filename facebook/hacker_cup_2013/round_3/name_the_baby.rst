Name the Baby
=============

Jack is blessed with a baby and he and his wife want to name their child. Jack
is a mathematician and his wife is very superstitious. She wants the baby's
name to contain at least one of her ancestors names as a substring. They have
decided that the baby's name should be exactly **L** characters long, and will
only consist of lowercase characters. Jack's wife gives Jack a list of **N**
strings, the names of her ancestors. Jack finds all the name possible names for
his baby and lists them in alphabetical order. He asks you to choose the **K**
th (1-based) name in the list as the name for his child.

Input
-----

The first line contains **T**, the number of test cases. Each test case begins
with the value of **L** followed by a single integer **K**. The next line
contains a single integer **N** followed by **N** lines, each containing the
name of one of the wife's ancestors.

Output
------

For every test case output the name for the child. If no such name exists print
"unnamed baby :(".

Constraints
-----------

1 ≤ **T** ≤ 20

1 ≤ **L** ≤ 100

1 ≤ **N** ≤ 100

1 ≤ length of each string in the list ≤ 100

1 ≤ **K** ≤ 10\ :sup:`18`

Example input
-------------

::

    5
    5 10
    2
    like
    poke
    5 100
    1
    hack
    3 5
    3
    ab
    bc
    ca
    7 100000
    4
    abcd
    bcde
    cdef
    defg
    10 1000000000
    5
    facebook
    hacker
    cup
    round
    three

Example output
--------------

::

    Case #1: epoke
    Case #2: unnamed baby :(
    Case #3: abd
    Case #4: dzdefgn
    Case #5: ajpxcccuph

`View online <https://www.facebook.com/hackercup/problems.php?pid=356563344451340&round=402976459784646>`_.
