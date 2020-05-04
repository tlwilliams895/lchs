Turtle Properties
=================

The ``turtle`` module contains methods that change the properties of either a
turtle object or the screen object.

Turtle Characteristics
----------------------

Once again, let's create a test turtle called ``bob`` and then explore how to
change its appearance.

.. sourcecode:: python
   :linenos:

   import turtle

   bob = turtle.Turtle()

.. figure:: ./figures/not-a-turtle.png
   :alt: Image showing the default Python turtle shape.

   Default turtle shape.

Shape
^^^^^

The Python library offers six choices for a turtle's shape---*'arrow', 'circle',
'classic', 'square', 'triangle',* and *'turtle'*. By default, turtles begin
with the *'classic'* shape.

.. figure:: ./figures/turtle-shapes.png
   :alt: Image showing the six shape options for Python turtles.

   Arrow, circle, classic, square, triangle, turtle.

To set the shape for ``bob``, we use the syntax:

.. sourcecode:: python

   turtle_name.shape('shape_name')

``shape_name`` must be one of the six options, and it must be in quotes. For
example, ``bob.shape('circle')`` changes ``bob`` from its default shape to a
circle.

.. figure:: ./figures/circle-turtle-line.png
   :alt: Image comparing the default drawing shape vs. a circle shape.

   Classic turtle shape + line vs. circle shape + line.

Line Width and Color
^^^^^^^^^^^^^^^^^^^^

To change the thickness of the lines drawn, use the syntax:

.. sourcecode:: python

   turtle_name.pensize(value)

``value`` can be any positive number.

To change the color of the lines, use the syntax:

.. sourcecode:: python

   turtle_name.color('color_name')

Python recognizes a large number of color names, which include standards like
*red, green, blue, cyan*, as well as options like *lightgreen, turquoise,
skyblue*, etc. The best way to tell if Python recognizes a color is to try!

.. index:: ! hex code

Python also accepts a **hex code** instead of a color name. A hex code is a
6-character code that describes how to mix different amounts of red, green, and
blue to produce a specific color. The code must follow a ``#`` character.

.. admonition:: Examples

   The following figure shows the result of giving ``bob`` different colors:

   .. sourcecode:: python
      :linenos:

      bob.pensize(3)                # Set the line thickness to 3 pixels.
      bob.color('red')
      bob.color('purple')
      bob.color('light salmon')     # Yeah, this is a color.
      bob.color('#3c79b8')          # Hex code for LaunchCode blue.

   .. figure:: ./figures/4-turtle-colors.png
      :alt: Image showing red, purple, light salmon and LaunchCode blue.

To see a list of color names that Python recognizes, check out the
`Trinket documentation <https://trinket.io/docs/colors>`__, which provides an
easy grid structure. If none of the colors shown appeal to you, remember that
hex codes allow you to tinker with the color until you find the exact shade you
want.

Fill Color
^^^^^^^^^^

To fill the design drawn by a turtle, use the syntax:

.. sourcecode:: python

   turtle_name.begin_fill()
   # Drawing code
   turtle_name.end_fill()

Lorem ipsum...

Drawing Speed
^^^^^^^^^^^^^

To set how quickly a turtle draws, use the syntax:

.. sourcecode:: python

   turtle_name.speed(speed_value)

``speed_value`` can be set to any integer from 1 (slowest) - 10 (fastest).
Setting ``speed_value`` to 0 skips the drawing animation and instantly shows
the finished shape on the screen.

Pen Control
-----------

Other methods determine when a turtle draws lines or leaves other marks on the
screen.

Penup and Pendown
^^^^^^^^^^^^^^^^^

Two methods control whether or not a turtle draws a line behind itself when it
moves:

.. sourcecode:: python

   turtle_name.penup()
   turtle_name.pendown()

The ``penup()`` method tells a turtle to lift up its tail. Any movement
commands that follow will reposition the turtle but NOT draw any lines.

The ``pendown()`` method does the opposite, drawing lines behind the turtle as
it moves. The ``pendown`` state is the default whenever a new turtle is
defined.

Stamp
^^^^^

The ``stamp()`` method leaves a print of the turtle's shape on the page.
Compare the results of the two code samples below. They both result in a line
that is 200 pixels long.

.. sourcecode:: python

   bob.forward(100)
   bob.forward(100)

   bob.stamp()
   bob.forward(100)
   bob.stamp()
   bob.forward(100)

INSERT FIGURE HERE!!!!

Notice how the second line shows where ``bob`` left an imprint (a stamp)
on the drawing before moving to the next position.

Screen Control
--------------

Lorem ipsum...
