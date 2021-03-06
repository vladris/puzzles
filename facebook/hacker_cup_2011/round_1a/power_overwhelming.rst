Power Overwhelming
==================

A lot of people at Facebook like to play Starcraft II™. Some of them have
made a custom game using the Starcraft II™ map editor. In this game, you play
as the noble Protoss defending your adopted homeworld of Shakuras from a
massive Zerg army. You must do as much damage to the Zerg as possible before
getting overwhelmed. You can only build two types of units, shield generators
and warriors. Shield generators do no damage, but your army survives for one
second per shield generator that you build. Warriors do one damage every
second. Your army is instantly overrun after your shield generators expire.
How many shield generators and how many warriors should you build to inflict
the maximum amount of damage on the Zerg before your army is overrun? Because
the Protoss value bravery, if there is more than one solution you should
return the one that uses the most warriors.

Input
-----

The first line of the input is the number of test cases, **N**. The next **N**
lines each contain a test case, which consists of three integers, **G**, **W**
and **M**, each separated by a single space. **G** is the cost to build a
shield generator. **W** is the cost to build a warrior. **M** is the total
amount of money you have to build warriors and shield generators.

Constraints
-----------

1 ≤ **G** ≤ 100

1 ≤ **W** ≤ 100

**G** + **W** ≤ **M** ≤ 1000000000000 (10\ :sup:`12`)

Output
------

For each test case, output a line containing a single integer **G**, the number
of shield generators you choose to build.

Example input
-------------

::

    5
    15 10 658931394179
    92 37 304080438521
    39 100 972826846685
    24 89 306549054135
    64 16 254854449271

Example output
--------------

::

    Case #1: 21964393379
    Case #2: 1652611083
    Case #3: 12472102915
    Case #4: 6386403897
    Case #5: 1991050385

`View online <https://www.facebook.com/hackercup/problems.php?pid=187006817978553&round=144428782277390>`_.
