Dance Battle
============

During an otherwise subdued night out on the town, you find yourself engaged in
a fierce dance battle with a formidable opponent. After a number of turns in
the battle have already been taken, both you and your adversary realize that
you are at risk of being made to look foolish on the dance floor and decide to
apply optimal strategy to the battle.

The rules of the battle are as follows: A turn consists of one battler executing
two moves, and the two battlers alternate turns. The first move made in a turn
must be the same as the second move the opponent made in the last turn. The
only exception to this rule is the first turn, where any move may be used to
start. Turns must be unique; once a pair of moves has been made in one turn
they cannot be used together again on another turn. Pairs are unordered so if
one dancer executes move 1 followed by move 2 in a single turn, neither dancer
can make moves 1 and 2 in the same turn in any order for the rest of the
battle. Dancers are allowed to make the same move twice during a turn. The
first dancer that cannot make a legal move is the loser.

Given the number of available moves and a list of turns that have already been
taken, and assuming both dancers will now pop the freshest (dance optimally),
your job is to determine who will win the battle. The first turn of every
battle is yours.

Input Specifications
--------------------

The input begins with two numbers **n** and **m** separated by newline
characters. **n** is the number of dance moves available. **m** is the number
of turns that were already taken in the battle. The file then continues with
**m** lines of the form:

::

    <a> <b>

Each line represents one turn that has already been taken in the dance battle,
where **a** is the first move made on that turn and **b** is the second. **a**
and **b** are separated by some number of tabs and spaces. The turns are listed
in the order they were taken. Moves are referenced by their zero-based indices,
so all  numbers listed will be between 0 and **n** - 1, inclusive. The last
line may or may not be followed by a newline character.

Example Input file:

::

    3
    2
    0 0
    0 1

Output Specifications
---------------------

Your output must consist of a single word followed by a newline character: "Win"
if you will win the dance battle and "Lose" if you will lose it.

Example Output:

::

    Win

Your program must be efficient in terms of time and memory required;
implementations lacking any insightful optimizations are likely to be
considered failures.
