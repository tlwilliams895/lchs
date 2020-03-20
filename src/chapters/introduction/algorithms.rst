Algorithms
==========

Have you ever alphabetized a stack of papers or a list of words? Did you sing
the alphabet song while you were performing the task? Did you sort the words
into groups based on the first letter? Did you "fan" the papers so you could
look at all of the names as you organized the stack? Did you get help from a
partner and split the task in half?

Regardless of how you completed the task, you probably followed a *pattern* to
make the process easier. If you had to repeat the task with a new set of words,
you could jump right in because you already had a system in place.

.. index:: ! algorithm

The word **algorithm** is just a fancy name for a pattern or set of steps.

Imagine a recipe for baking cookies. After the list of ingredients comes a
series of step-by-step instructions for making the treats. If you want to cook
something else, like a cake or a roast, you follow a different set of steps
using a different set of ingredients.

An *algorithm* is like a recipe. It is a careful series of steps that, when
followed, produce a specific result. Programmers create algorithms to solve
small tasks. By combining the answers from these small tasks, programmers can
solve much larger problems.

Let's take a look at an example of an algorithm---alphabetizing a list of
words:

``apple, pear, zebra, box, rutabaga, fox, banana, socks, foot``

One possible set of steps for solving the task could be:

#. Arrange the words from a - z based only on the first letter:

   ``apple, box, banana, fox, foot, pear, rutabaga, socks, zebra``

#. If more than one word starts with 'a', rearrange those words based on the
   second letter. Repeat for the words that start with 'b', then 'c', etc.:

   ``apple, banana, box, fox, foot, pear, rutabaga, socks, zebra``

#. If multiple words start with 'a' and have the same second letter, rearrange
   those words based on the third letter. Repeat for the 'b' words, then the
   'c' words, etc.:

   ``apple, banana, box, foot, fox, pear, rutabaga, socks, zebra``

#. If other repeats exist, continue sorting the list by comparing the 4th, 5th,
   6th letters (etc.) until all the words are properly arranged.

This is not the ONLY way to solve the task, but it provides a series of steps
that can be used in many different situations to organize different lists of
words.

Alphabetizing is a process we can teach a computer to do, and the algorithm
will complete the process much more rapidly than a human. However, unlike the
alphabet song that many of us still sing in our heads when arranging a list of
words, programmers must use a different method to train the computer.

Check Your Understanding
-------------------------

.. admonition:: Question

   Select ALL of the following that can be solved by using an algorithm:

   a. Answering a math problem.
   b. Sorting numbers in decreasing order.
   c. Making a peanut butter and jelly sandwich.
   d. Assigning guests to tables at a wedding reception.
   e. Creating a grocery list.
   f. Suggesting new music for a playlist.
   g. Making cars self-driving.
