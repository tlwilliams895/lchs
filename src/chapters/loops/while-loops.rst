``while`` Loops
===============

.. index:: ! while

.. index::
   single: loop; while

There is another Python keyword that can also be used for iteration---
**while**. A ``while`` loop is similar to an ``if`` statement because it uses
a boolean expression to control the iteration. The body of the ``while`` loop
repeats as long as the boolean expression evaluates to ``True``.

``while`` Loop Syntax
---------------------

The general syntax of a ``while`` loop looks like this:

::

   while boolean expression:
      loop body

A ``while`` loop continues to repeat as long as the boolean expression
evaluates to ``True``. This *condition* usually includes a value or variable
that is updated within the loop. Eventually, the condition becomes ``False``,
and the loop stops.

.. admonition:: Example

   The following loop repeats until ``total < 1000`` returns ``False``:

   .. sourcecode:: Python

      total = 0
      increase_by = 14

      while total < 1000:
         total += increase_by

``for`` vs. ``while``
---------------------

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

For example, let's say we want a user to enter their ID number. We can use
an ``input`` statement to prompt the user for the information and then check
if the number is valid. If the user makes a mistake, we want to prompt them for
their number again.

We cannot know ahead of time how many tries the user will need. Since a ``for``
loop repeats a specific number of times, it will not work for this case.
Instead, a ``while`` loop works better. Whether the user needs 1, 2, 10, or
more tries, the loop operates only as long as it has to.

.. index:: ! indefinite iteration

**Indefinite iteration** refers to the case when we do not know how many times
a loop needs to repeat.

.. TODO: Add internal link here leading back to the boolean expressions section.


.. TODO: Define **definite iteration** vs. indefinite iteration. Definite
   iteration is the process of repeating a specific task with a specific data
   set.
