Which Loop To Use?
==================

.. index:: ! definite iteration

Each time we write a ``for`` statement, we tell Python *exactly* how many times
the loop body must repeat. ``for char in "Hello"`` repeats once for each letter
in the string (5 times). Similarly, ``for value in range(10)`` repeats 10
times, with ``value`` assigned the numbers 0 - 9.

Even when we use variables in ``range(start, stop, step)``, these variables
store specific vales. Python knows *exactly* how many times to repeat the loop
body, and this is called **definite iteration**. The starting and ending points
of are set inside the ``for`` statement.

When we write a ``while`` loop, we give Python a condition to evaluate. When
the condition returns ``False``, the loop stops. We do NOT need to know how
many times to repeat the loop. It will keep going as long as necessary.

As we saw in the input validation example, we cannot not know ahead of time how
many tries the user will need. Since a ``for`` loop repeats a specific number
of times, it will not work for this case. Instead, a ``while`` loop works
better. Whether the user needs 1, 2, 10 (or more) tries, the loop operates only
as long as it has to.

.. index:: ! indefinite iteration

**Indefinite iteration** refers to the case where we do not know how many times
a loop needs to repeat.

So which type of loop should we use in our code? ``for`` loops do better when
iterating over a collection or a fixed number of times. For the cases when
``for`` loops do not work, ``while`` loops get the job done.

Here are some points of comparison between the two types of loops.

``for`` Pros and Cons
^^^^^^^^^^^^^^^^^^^^^

#. Easier to set up than ``while`` loops.
#. Must have a definite start and end point, and these must be declared in the
   ``for`` statement.
#. Can loop through strings and collections without using an index value (e.g.
   ``for char in 'hello':``).
#. Automatically updates the loop variable.
#. Kinda hard to accidentally create an infinite Python ``for`` loop.
#. Can be used in place of some ``while`` loops, but not all.
#. Do not work for input validation.

``while`` Pros and Cons
^^^^^^^^^^^^^^^^^^^^^^^

#. More flexible than ``for`` loops.
#. ANY ``for`` loop can be re-written as a ``while`` loop.
#. Do not need to know beforehand how many times the loop needs to run.
#. Can be used for input validation.
#. ``while`` loops require more work to build.
#. Making an infinite ``while`` loop is easy.

Check Your Understanding
------------------------

.. admonition:: Question

   You are asked to program a robot to move tennis balls from one box (Box #1) to another (Box #2), one-by-one. The robot should continue moving balls until Box #1 is empty, and balls may be added to the box after the robot begins its work.

   Which type of loop should you use to write the program?

   #. ``while`` loop
   #. ``for`` loop

.. admonition:: Question

   You are asked to write a program similar to the one above, with the modification that a user may give the robot a specific number of balls to move from Box #1 to Box #2. (You can assume there will always be more balls than the user has asked the robot to move.)

   Which type of loop should you use to write the program?

   #. ``while`` loop
   #. ``for`` loop
