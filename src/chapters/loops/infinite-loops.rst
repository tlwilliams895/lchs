Infinite Loops
==============

Here's the code for a simple while loop.

   INSERT REPL HERE!!!!

Remove ``num += 1`` from the code and run the program.

.. sourcecode:: python
   :linenos:

   num = 0

   while num < 21:
      print(num)
      num += 1

Yikes!!! What happened? The program just keeps running!

.. index:: ! infinite loop

This is an example of an **infinite loop**, which is a set of code that repeats
forever. By removing ``num += 1`` from the loop body, the value of the variable
remains 0. The condition ``num < 21`` will ALWAYS be ``True``, so the loop will
NEVER stop.

Coding Infinity
---------------

Simple mistakes in the code create infinite loops, and *every* programmer
accidentally creates one from time to time. Consider it a rite of
passage---when you launch your first, welcome to the club.

.. admonition:: Tip

   When this happens to you, typing ``control-c`` will usually force your
   program to stop.

Infinite loops are usually created from small typos or missing statements.
These mistakes set up a situation where the ending condition cannot be reached.

.. admonition:: Examples

   Here's another infinite while loop. The program is supposed to print a
   decreasing total until that total reaches 0.

   .. sourcecode:: python
      :linenos:

      start_value = 26
      total = start_value

      while start_value > 0:
         total -= 5
         print(total)
   
   In this case, the update statement is present (line 5), but the error occurs
   in line 4. Instead of using ``total`` in the boolean expression, we used
   ``start_value``, which never gets updated in the loop.

   Here's an example of an infinite ``for`` loop in Python:

   .. sourcecode:: python
      :linenos:

      # NOPE! Nothing to see here!

   Well. That's nice.
   
   Although it *is* possible to create an infinite ``for`` loop in Python, you
   need to be very deliberate and think very hard about how to make it happen.
   You are unlikely to create one by accident.

Fun Fact
--------

Infinite loops are such an established part of programming that Apple even
made one the address of its California campus.

.. figure:: figures/infinite-loop-street.jpg
   :alt: Apple campus, 1 Infinite Loop, Cupertino, CA 95014
   
   1 Infinite Loop, Cupertino, CA

Check Your Understanding
------------------------

.. admonition:: Question

   The following code contains an infinite loop. Which is the BEST explanation
   for why the loop does not end?

   .. sourcecode:: python
      :linenos:

      num = 10
      answer = 1

      while num > 0:
         answer = answer + num
         num += 1

      print(answer)

   #. ``num`` starts at 10 and is increases by 1 each time through the loop, so
      it will always be positive
   #. ``answer`` starts at 1 and increases by ``num`` each time, so it will
      always be positive
   #. You cannot compare ``num`` to 0 in a ``while`` loop. You must compare it
      to another variable.
