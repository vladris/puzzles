Slot Machine Hacker
===================

You recently befriended a guy who writes software for slot machines. After
hanging out with him a bit, you notice that he has a penchant for showing off
his knowledge of how the slot machines work. Eventually you get him to describe
for you in precise detail the algorithm used on a particular brand of machine.
The algorithm is as follows:

::

    int getRandomNumber() {
      secret = (secret * 5402147 + 54321) % 10000001;
      return secret % 1000;
    }

This function returns an integer number in [0, 999]; each digit represents one
of ten symbols that appear on a wheel during a particular machine state.
**secret** is initially set to some nonnegative value unknown to you.

By observing the operation of a machine long enough, you can determine value of
**secret** and thus predict future outcomes. Knowing future outcomes you would
be able to bet in a smart way and win lots of money.

Input
-----

The first line of the input contains positive number **T**, the number of test
cases. This is followed by **T** test cases. Each test case consists of a
positive integer **N**, the number of observations you make. Next **N** tokens
are integers from 0 to 999 describing your observations.

Output
------

For each test case, output the next 10 values that would be displayed by the
machine separated by whitespace.

If the sequence you observed cannot be produced by the machine your friend
described to you, print "Wrong machine" instead.

If you cannot uniquely determine the next 10 values, print "Not enough
observations" instead.

Constraints
-----------

**T** = 20

1 ≤ **N** ≤ 100

Tokens in the input are no more than 3 characters long and contain only digits 0-9.

Example input
-------------

::

    5
    1 968
    3 767 308 284
    5 78 880 53 698 235
    7 23 786 292 615 259 635 540
    9 862 452 303 558 767 105 911 846 462

Example output
--------------

::

    Case #1: Not enough observations
    Case #2: 577 428 402 291 252 544 735 545 771 34
    Case #3: 762 18 98 703 456 676 621 291 488 332
    Case #4: 38 802 434 531 725 594 86 921 607 35
    Case #5: Wrong machine

`View online <https://www.facebook.com/hackercup/problems.php?pid=102490243159137&round=167482453296629>`_.
