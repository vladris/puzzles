﻿Labelmaker
==========

David is labelling boxes in a giant warehouse. He has a *lot* of boxes to
label, but unfortunately his labeling machine is broken, so only some of the
letters work. In order to be efficient, David labels the boxes by first using
every possible 1-letter label in alphabetical order, then using every possible
2-letter label in alphabetical order, then every 3-letter label, etc.

For example, suppose only the letters 'D', 'T', and 'Z' work. David would label
the first 15 boxes as follows: D, T, Z, DD, DT, DZ, TD, TT, TZ, ZD, ZT, ZZ,
DDD, DDT, DDZ. The first box is considered box #1, not box #0.

Given a set of working letters **L** on David's labelling machine and a number
**N** of boxes to label, return the label on the last box.

Input
-----

The first line of the input consists of a single integer **T**, the number of
test cases. Each test case consists of the string **L** and the integer **N**,
separated by a space.

Output
------

For each test case **i** numbered from 1 to **T**, output "Case #i: ", followed
by the label on the last box.

Constraints
-----------

1 ≤ **T** ≤ 20

1 ≤ length(**L**) ≤ 25

**L** will be in alphabetical order, consist of only uppercase letters A-Z, and
contain each letter at most once

1 ≤ **N** ≤ 2\ :sup:`63`-1

The test cases will be designed so that no label is longer than 50 letters

Example input
-------------

::

    5
    EHT 34
    ABCEFKO 4296473
    ACEHKMPRTU 4125383079316
    CDEGHIKLOSUWY 8333092520403744490
    ADEFHNOPSUVY 3365973428406169086

Example output
--------------

::

    Case #1: THE
    Case #2: FACEBOOK
    Case #3: HACKERCUPTEAM
    Case #4: WISHESYOUGOODLUCK
    Case #5: ANDHOPESYOUHAVEFUN

`View online <https://www.facebook.com/hackercup/problems.php?pid=637270059647812&round=1437956993099239>`_.
