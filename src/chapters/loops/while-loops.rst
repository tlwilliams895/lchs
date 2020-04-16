``while`` Loops
===============

.. index:: ! while

.. index::
   single: loop; while

There is another Python keyword that can also be used for iteration---``while``.
Unlike a ``for`` loop, which defines a loop variable and a specific starting
and ending point, a **while loop** uses a single condition to determine whether
or not to continue running.

This condition (a boolean expression) controls the iteration. The body of a
``while`` loop repeats as long as the expression evaluates to ``True``.

.. TODO: Add internal link here leading back to the boolean expressions section.

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

Just like with ``for`` loops, the body of a ``while`` loop must be indented,
and it may contain any number of statements.

.. admonition:: Example

   The following loop repeats until ``total < 1000`` returns ``False``:

   .. sourcecode:: Python

      total = 0
      increase_by = 14

      while total < 1000:
         total += increase_by
         print(total)

Control Flow
------------

We can visualize the program flow of a ``while`` loop as follows.

   INSERT FIGURE HERE!!!!

   Flow of execution of a ``while`` loop

#. Python evaluates the condition, which returns a value of ``True`` or
   ``False``.
#. If the condition is ``False``, exit the ``while`` loop and continue
   the program at the next statement after the loop body.
#. If the condition is ``True``, run the loop body and then go back to step 1.

``for`` Loops Rewritten as ``while`` Loops
------------------------------------------

We can use ``while`` to create any type of loop we want, including anything we
previously did with a ``for`` loop. For example, consider our first ``for``
loop that printed the numbers 0 - 20:

.. sourcecode:: python
   :linenos:

   for num in range(21):
      print(num)

This can be rewritten as a while loop:

.. sourcecode:: python
   :linenos:

   num = 0

   while num < 21:
      print(num)
      num += 1

Instead of using the ``range`` function to produce the values for ``num``, we
need to produce them ourselves in a ``while`` loop. To do this, *before*
starting the loop, we create the variable ``num`` and assign it a value of
``0``. Every iteration, line 5 increases ``num`` by 1. Eventually, ``num``
increases enough to make the condition ``num < 21`` false, and the loop ends.

``num`` plays the same role as the loop variable in the ``for`` loop, but we
need to manage its value ourselves. The ``for`` and ``while`` loops in the
examples above do *exactly* the same thing, but they solve the task slightly
differently.

If we imagine giving instructions to someone, the ``for`` and ``while``
approaches might sound something like:

#. **For**: Repeat this task for each number 0 - 20.
#. **While**: Repeat this task as long as the number is less than 21.

Try It!
^^^^^^^

Convert for loop into the equivalent while...

   INSERT REPL HERE!!!!

Input Validation
----------------

``while`` loops require a little more effort to code than ``for`` loops, but
``while`` loops tend to be more flexible.

We can replace ANY ``for`` loop with a ``while``, but the reverse is NOT true.
Many ``while`` loops can be converted into ``for`` loops, but there are some
instances where only a ``while`` loop will work. Let's look at one example of
this.

.. index:: ! input validation

This program is an example of **input validation**. It prompts the user to
enter a positive number. If the user enters ``0`` or any negative number, then
they see an error message and are prompted again within the body of the loop.
If the user keeps entering invalid numbers, the loop continues to iterate. As
soon as the user chooses a valid number, the loop ends.

   INSERT REPL HERE!!!

.. sourcecode:: python
   :linenos:

   num_choice = 0

   while num_choice <= 0:
      num_choice = int(input('Choose a positive number: '))
      if num_choice <= 0:
         print('Invalid number')

This example shows the additional flexibility provided by ``while`` loops.
``for`` loops iterate a specific number of times, but in this case we have no
way of knowing how many times we need to prompt the user for a number. By
setting a single condition (``num_choice <= 0``) we can keep the ``while`` loop
going until the condition returns ``False``.

Check Your Understanding
------------------------

Lorem ipsum...
