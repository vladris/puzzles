Hold'em Numbers
===============

In the game of Hold'em Numbers, 4 players play with a deck of **N** cards, where
each card has a distinct number from the range [1 .. **N**] on it. Each player 
is dealt two cards and the player who has the highest sum of the two numbers 
wins. If multiple players have the highest sum, the one of them who holds the 
highest card wins. All 8 cards are dealt simultaneously so it's impossible for 
two players to have the same card.

After seeing your two cards you can bet $1. If you win the hand you get $4 back
but if another player wins you lose your dollar. You can also fold, in which
case you don't win nor lose any money. Your opponents play very aggressively and
they will always bet. After the winner is determined all cards are reshuffled to
play another hand for the total of **H** games. It's possible you get dealt the 
same hand more than once.

You want to maximize your winnings and only bet if your expected winnings are
strictly greater than zero. To help yourself you decided to write a program that
for the given deck size and hands you were dealt returns whether you should bet
or fold.

Input
-----

The first line of the input consists of a single integer **T**, the number of test
cases. 

Each test case starts with a line containing two integers **N** and **H**

The subsequent **H** lines each contain two integers, **C1** and **C2**, the 
cards you were dealt.

Output
------

For each test case i numbered from 1 to **T**, output "Case #i: ", followed by a
string of **H** characters. Each character being either "B" if you should bet,
or "F" if should fold. The order of characters corresponds to the order of
hands given in the input.

Constraints
-----------

1 ≤ **T** ≤ 20 

8 ≤ **N** ≤ 100 

1 ≤ **H** ≤ 10000 

1 ≤ **C1**, **C2** ≤ **N** 

**C1** != **C2**

Examples
--------

In the first three examples we are playing a single hand with a deck of eight
cards. The first case is a clear winner so you should bet. The second case gives
no chance to win and you should fold. Finally the third case gives you 40%
chance of winning. This is good enough to make the bet profitable.

Example input
-------------

::

    5
    8 1
    7 8
    8 1
    1 2
    8 1
    7 4
    11 2
    6 9
    9 6
    12 3
    6 9
    11 5
    9 6

Example output
--------------

::

    Case #1: B
    Case #2: F
    Case #3: B
    Case #4: BB
    Case #5: FBF

`View online <https://www.facebook.com/hackercup/problems.php?pid=527868440642335&round=544142832342014>`_.
