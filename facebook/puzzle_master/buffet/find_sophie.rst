Find Sophie
===========

After a long day of coding, you love to head home and relax with a loved one.
Since that whole relationship thing hasn't been working out for you recently,
that loved one will have to be your cat, Sophie. Unfortunately you find
yourself spending considerable time after you arrive home just trying to find
her. Being a perfectionist and unable to let anything suboptimal be a part of
your daily life, you decide to devise the most efficient possible method for
finding Sophie.

Luckily for you, Sophie is a creature of habit. You know where all of her
hiding places are, as well as the probability of her hiding in each one. You
also know how long it takes you to walk from hiding place to hiding place.
Write a program to determine the minimum expected time it will take to find
Sophie in your apartment. It is sufficient to simply visit a location to check
if Sophie is hiding there; no time must be spent looking for her at a
location. Sophie is hiding when you enter your apartment, and then will not
leave that hiding place until you find her. Your program must take the name of
an input file as an argument on the command line.

Input Specifications
--------------------

The input file starts with a single number, m, followed by a newline. m is the
number of locations available for Sophie to hide in your apartment. This line
is followed by m lines, each containing information for a single location of
the form (brackets for clarity):

::

    <location name> <probability>

probability is the probability that Sophie is hiding in the location indicated.
The sum of all the probabilities is always 1. The contents of these lines are
separated by whitespace. Names will only contain alphanumeric characters and
underscores ('_'), and there will be no duplicate names. All input is
guaranteed to be well-formed. Your starting point is the first location to be
listed, and in effect it costs you no time to check if Sophie is there.

The file continues with a single number, c, followed by a newline. c is the
number of connections that exist between the various locations. This line is
followed by c lines, each of the form:

::

    <location name> <location name> <seconds>

The first two entries are the names of locations and seconds is the number of
seconds it takes you to walk between the them. Again these lines are
whitespace-delimited. Note that the locations are unordered; you can walk
between them in either direction and it will take the same amount of time. No
duplicate pairs will be included in the input file, and all location names will
match one described earlier in the file.

Example input file:

::

    4
    front_door .2
    in_cabinet .3
    under_bed .4
    behind_blinds .1
    5
    front_door under_bed 5
    under_bed behind_blinds 9
    front_door behind_blinds 5
    front_door in_cabinet 2
    in_cabinet behind_blinds 6

Output Specifications
---------------------

Your output must consist of a single number followed by a newline, printed to
standard out. The number is the minimum expected time in seconds it takes to
find Sophie, rounded to the nearest hundredth. Make sure that the number
printed has exactly two digits after the decimal point (even if they are
zeroes). If it is impossible to guarantee that you will find Sophie, print
"-1.00" followed by a newline instead.

Example output:

::

    6.00

