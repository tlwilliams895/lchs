Project: Loops
==============

Let's use Python turtles to practice writing loops!

Part A - Polygons and Sprites
-----------------------------

In the chapter, you coded a program to make a turtle draw a *regular polygon*
(a shape with all the sides the same length and all the angles the same).

.. sourcecode:: Python
   :linenos:

   import turtle

   bob = turtle.Turtle()

   num_sides = 8

   turn_angle = 360.0 / num_sides

   for side in range(num_sides):
      bob.forward(50)
      bob.left(turn_angle)

#. Modify the program to prompt the user to enter the number of sides for the
   polygon.
#. Modify the program to ask the user to enter the length for each side.

   .. admonition:: Tip

      ``bob.color('blue')`` changes the color of the lines to blue. Many color
      choices are available. Feel free to play with this feature.

      You can also fill the polygon with a color. Refer to the Turtle Appendix
      for details.

         INSERT INTERNAL LINK HERE!!!!!

.. TODO: Insert internal link here.

A *sprite* is a simple spider shaped thing with a certain number of legs coming
out from a center point.

   INSERT SPRITE IMAGES AND GIF HERE!!!

3. Write a program to draw a sprite, where the number of legs is provided by
   the user. You will need to use a variable to hold the turn angle for the
   turtle.

Part B - Clock Face
-------------------

Entering a value of ``12`` for your sprite draws something like a clock face:

   INSERT IMAGE HERE!!!!

#. Use the ``.penup()`` and ``.pendown()`` methods in your loop to make the
   drawing look like this:

      INSERT IMAGE HERE!!!!

#. Finally use the ``.stamp()`` method to make a mark at the end of each line.
   Your final output should look like this:

      INSERT IMAGE HERE!!!!

Part C - Nested Loops
---------------------

.. index::
   single: loop; nested

.. index:: ! nested loops

**Nested loops** occur when one loop is placed inside of another. For one
iteration of the *outer loop*, the *inner loop* completes ALL of its
iterations.

.. admonition:: Example

   INSERT REPL HERE!!!!

   .. sourcecode:: Python
      :linenos:

      for step in range(3):
         print("Iteration", step+1, "of the outer loop.")

         for turn in range(3):
            print("Iteration", turn+1, "of the inner loop.")
         
         print("---")

Let's use a nested loop to draw three sprites in a row.

#. Modify your sprite code to make it the an inner loop. The outer loop should
   look something like:

   .. sourcecode:: Python
      :linenos:

      for sprite in range(3):
         turtle_name.penup()
         turtle_name.forward(100)  # Feel free to change this length.
         turtle_name.pendown()

         # Your sprite loop here.

#. Modify your program to prompt the user to enter the number of sprites to
   draw.

Part D - Bring it Together
--------------------------

Lorem ipsum...
