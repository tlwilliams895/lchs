Turtle Properties
=================

Once again, let's create a test turtle called ``bob`` and then explore how to
change its appearance.

.. sourcecode:: python
   :linenos:

   import turtle

   bob = turtle.Turtle()

.. figure:: ./figures/not-a-turtle.png
   :alt: Image showing the default Python turtle shape.

   Default turtle shape.

The ``turtle`` module contains methods that change the properties of either the
turtle object or the screen object. The table below lists the common methods
used to change the look of what gets drawn. Clicking on any of the keywords
leads to a more detailed description.

.. list-table:: Common Turtle Methods
   :header-rows: 1

   * - Drawing
     - Pen Control
     - Screen Control
   * - :ref:`color() <turtle-color>`
     - :ref:`pensize() <pen-size>`
     - :ref:`setup() <screen-setup>`
   * - :ref:`shape() <turtle-shape>`
     - :ref:`penup() <pen-up-down>`
     - :ref:`bgcolor() <screen-background-color>`
   * - :ref:`speed() <turtle-speed>`
     - :ref:`pendown() <pen-up-down>`
     - :ref:`title() <screen-title>`
   * - :ref:`fillcolor() <turtle-fill>`
     - :ref:`clear() <pen-clear-reset>`
     - :ref:`exitonclick() <screen-exit>`
   * - :ref:`begin_fill() end_fill() <turtle-fill-shape>`
     - :ref:`reset() <pen-clear-reset>`
     - 
   * - :ref:`stamp() <turtle-stamp>`
     - 
     - 

Feel free to experiment with the methods in the three editors below:
:ref:`drawing <draw-try>`, :ref:`pen control <pen-try>`,
:ref:`screen control <screen-try>`.

Drawing Methods
---------------

Besides movement commands like ``forward`` and ``left``, we can also change the
characteristics of the turtle object.

.. _turtle-color:

Turtle Color
^^^^^^^^^^^^

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

.. admonition:: Example

   The following figure shows the result of giving ``bob`` different colors:

   .. sourcecode:: python
      :lineno-start: 5

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
hex codes let you tinker with the color until you find the exact shade you
want.

.. _turtle-fill:

Fill Color
~~~~~~~~~~

Turtles can also fill the shapes they draw with a particular color. By default,
the fill color and line color are the same, so ``bob.color('blue')`` draws blue
lines and fills shapes with that color.

To change the fill color, use the syntax:

.. sourcecode:: python

   turtle_name.fillcolor('color_name')

Just like with the ``color`` method, ``fillcolor`` recognizes specific color
names, and it also accepts hex codes. Note that the line and fill colors are
both represented by the turtle image on the screen.

.. admonition:: Examples

   The following figure shows the result of giving ``bob`` different fill
   colors. In each case, the line color is black.

   .. sourcecode:: python
      :lineno-start: 5

      bob.pensize(3)                # Set the line thickness to 3 pixels.
      bob.fillcolor('violet')
      bob.fillcolor('yellow')
      bob.fillcolor('white smoke')  # Yeah, this is a color.
      bob.fillcolor('#419f6a')      # Hex code for LaunchCode green.

   .. figure:: ./figures/4-fill-colors.png
      :alt: Image showing violet, yellow, white smoke and LaunchCode blue fill colors.

.. admonition:: Tip

   We can use the ``color`` method to set BOTH the line and fill color by
   using two parameters instead of one.

   .. sourcecode:: python
      :lineno-start: 5

      bob.pensize(3)                      # Set the line thickness to 3 pixels.
      bob.color('black', 'pink')          # Set black line color and pink fill color.
      bob.color('purple', 'gold')
      bob.color('tomato', 'skyblue')
      bob.color('#3c79b8', '#419f6a')     # Hex codes for LaunchCode blue and green.

   .. figure:: ./figures/4-line-fill-colors.png
      :alt: Image showing 4 examples of setting line and fill colors.

.. _turtle-shape:

Turtle Shape
^^^^^^^^^^^^

The Python library offers six choices for a turtle's shape---*'arrow', 'circle',
'classic', 'square', 'triangle',* and *'turtle'*. By default, turtles begin
with the *'classic'* shape.

.. figure:: ./figures/turtle-shapes.png
   :alt: Image showing the six shape options for Python turtles.

   Arrow, circle, classic, square, triangle, turtle.

To set the shape for a turtle object, we use the syntax:

.. sourcecode:: python

   turtle_name.shape('shape_name')

``shape_name`` must be one of the six options, and it must be in quotes. For
example, ``bob.shape('circle')`` changes ``bob`` from its default shape to a
circle.

.. figure:: ./figures/circle-turtle-line.png
   :alt: Image comparing the default drawing shape vs. a circle shape.

   Classic turtle shape + line vs. circle shape + line.

.. _turtle-speed:

Turtle Speed
^^^^^^^^^^^^

To set how quickly a turtle draws, use the syntax:

.. sourcecode:: python

   turtle_name.speed(speed_value)

``speed_value`` can be set to any integer from 1 (slowest) - 10 (fastest).
Setting ``speed_value`` to 0 skips the drawing animation and instantly shows
the finished shape on the screen.

.. _turtle-fill-shape:

Fill a Shape
^^^^^^^^^^^^

To fill the design drawn by a turtle, use the syntax:

.. sourcecode:: python

   turtle_name.begin_fill()
   # Drawing code
   turtle_name.end_fill()

Lorem ipsum...

.. _turtle-stamp:

Making a Stamp
^^^^^^^^^^^^^^

The ``stamp()`` method leaves a print of the turtle's shape on the page.
Compare the results of the two code samples below. They both result in a line
that is 200 pixels long.

.. sourcecode:: python
   :linenos:

   bob.forward(100)
   bob.forward(100)

   bob.stamp()
   bob.forward(100)
   bob.stamp()
   bob.forward(100)

INSERT FIGURE HERE!!!!

Notice how the second line shows where ``bob`` left an imprint (a stamp)
on the drawing before moving to the next position.

.. _draw-try:

Try It! (Drawing)
^^^^^^^^^^^^^^^^^

   INSERT REPL HERE!!!!

Focus should be on turtle appearance.

Pen Control
-----------

Other methods determine when a turtle draws lines or leaves other marks on the
screen.

.. _pen-size:

Line Thickness (Pen Size)
^^^^^^^^^^^^^^^^^^^^^^^^^

To change the thickness of the lines drawn, use the syntax:

.. sourcecode:: python

   turtle_name.pensize(value)

``value`` sets the number of pixels, and it can be any positive number. The
larger the value, the thicker the lines. By default, turtles start with a
pensize of 1.

.. _pen-up-down:

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

.. _pen-clear-reset:

Clear and Reset
^^^^^^^^^^^^^^^

Lorem ipsum...

.. _pen-try:

Try It! (Pen)
^^^^^^^^^^^^^

   INSERT REPL HERE!!!!

Try drawing a dashed line, a stamped line, thick and thin lines, steadily
increasing lines, etc.

Screen Control
--------------

Lorem ipsum...

.. _screen-setup:

Set Up
^^^^^^

Lorem ipsum...

.. _screen-background-color:

Background Color
^^^^^^^^^^^^^^^^

Lorem ipsum...

.. _screen-title:

Title
^^^^^

Lorem ipsum...

.. _screen-exit:

Exit On Click
^^^^^^^^^^^^^

Lorem ipsum...

.. _screen-try:

Try It! (Screen)
^^^^^^^^^^^^^^^^

   INSERT REPL HERE!!!!

Try opening a small/large window, green background, and a unique title.
