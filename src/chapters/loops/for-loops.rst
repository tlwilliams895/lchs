``for`` Loops
=============

If you were to instruct your pet turtle to draw a square in the sand, your
commands would quickly become quite tedious. You must tell your pet to move
then turn, move then turn, etc. four times. If you want your turtle to draw a
hexagon, an octagon, or a polygon with 42 sides, it would be a nightmare to
repeat all the commands!

.. admonition:: Example

   Turtle statements for drawing a square:

   .. sourcecode:: python
      :linenos:

      import turtle

      pet = turtle.Turtle()

      pet.forward(50)
      pet.left(90)
      pet.forward(50)
      pet.left(90)
      pet.forward(50)
      pet.left(90)
      pet.forward(50)
      pet.left(90)

   Note: If you have not practiced with turtles in class yet, check out the
   :ref:`Python Turtles <turtle-guide>` appendix.

A basic building block of all programs is to repeat some code over and over
again, which we call *iteration*. The first Python iteration tool we will learn
is the ``for`` loop. 

``for`` Loop Syntax
-------------------

.. index::
   single: loop; for

.. index:: ! for loop

A **for loop** repeats a specific set of code statements a specific number of
times. When a ``for`` loop begins, we must declare exactly how many times it
will run.

Play around with the basic syntax of a ``for`` loop.

.. admonition:: Try It

   This program prints the integers 0 through 20, one number per line.

   .. raw:: html

      <iframe height="400px" width="100%" src="https://repl.it/@launchcode/LCHS-Basic-Python-Loop?lite=true" scrolling="no" frameborder="yes" allowtransparency="true"></iframe>
   
   #. What do you notice about the numbers printed in the console vs. the
      value inside ``range()``?
   #. Try changing the value inside ``range()``. What values throw an error?
   #. What happens when you indent line 4 to match line 2?

Let's break down the syntax piece by piece, so we can begin to understand how
``for`` loops are structured.

.. index::
   single: for loop; variable

#. In line 1, ``num`` is called the **loop variable**. Each time the loop
   executes, ``num`` gets assigned a new value.
#. Line 2 begins the loop body. The loop body is ALWAYS indented. The
   indentation determines exactly what statements are “in the loop”. You saw
   this when you indented line 4 to match line 2. Originally, line 4 was
   outside of the loop and ran only once. By indenting line 4, it becomes part
   of the loop body and gets repeated multiple times.
#. The *first* unindented line after the ``for`` statement marks the end of the
   loop body.
#. The loop body can contain any number of statements.
#. The number of times the loop body runs depends on the value in ``range()``.

Line By Line
^^^^^^^^^^^^

Let's modify the code just a little to follow the operation of a ``for`` loop.

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      for num in range(4):
         print(num)
         print("Hello" * num)

      print("Done!")

   **Console Output**

   ::

      0

      1
      Hello
      2
      HelloHello
      3
      HelloHelloHello
      Done!

#. The first time Python executes the ``for`` statement in line 1, ``num`` is
   assigned a value of ``0``.
#. Line 2 executes, printing the current value of ``num``.
#. Line 3 executes, printing the string ``Hello`` zero times.
#. Python reaches the end of the loop body (the indented lines) and then MOVES
   BACK TO THE ``for`` STATEMENT (line 1).
#. Since the current value of ``num`` has not reached the end of the specified
   ``range``, ``num`` gets reassigned to the next higher value (``1``).
#. Lines 2 and 3 execute again, using the new value of ``num``. ``1`` and
   ``Hello`` get printed.
#. Python again reaches the end of the loop body and moves back up to the
   ``for`` statement. ``num`` gets reassigned a value of ``2``.
#. This process continues until the value of ``num`` reaches the end of the
   specified ``range``.
#. Once the loop finishes, Python proceeds to line 5.

Notice that even though line 1 uses ``range(4)``, the value ``4`` is NOT
included in the output. Why?

Begin Counting at 0
^^^^^^^^^^^^^^^^^^^

.. index:: ! zero-based indexing

Iterating a certain number of times is a very common thing to do, and Python
gives us a special built-in ``range`` keyword that provides a sequence of
values for the for loop variable to use.

The sequence provided by ``range`` always starts with ``0``. If you ask for
``range(4)``, then you will get 4 values starting with 0. In other words, 0, 1,
2, and finally 3. Notice that 4 is not included since we started with 0.
Likewise, ``range(10)`` provides 10 values, 0 through 9. Starting a count at 0
instead of at 1 is called **zero-based indexing** and is very common in
computer programming.

.. admonition:: Note

   Programmers like to count from 0!

   For ``range(n)``, the loop variable will take each integer value from 0 up
   to BUT NOT INCLUDING ``n``.

Try It!
-------

Take a look at the turtle code at the top of this page. Which statements are
repeated? How many times?

Complete the code below by entering a value into ``range``. Next, copy and
paste the SMALLEST number of statements into the loop body that will make the
turtle draw a square. Don't forget to indent!

.. raw:: html

   <iframe height="400px" width="100%" src="https://repl.it/@launchcode/LCHS-Turtle-Square?lite=true" scrolling="no" frameborder="yes" allowtransparency="true"></iframe>
