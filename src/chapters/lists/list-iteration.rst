Iterating Through Lists
=======================

Just like with strings, we can use a loop to iterate through the elements in a
list.

Loop by Element
---------------

Since a list is simply a sequence of separate data values, Python gives us a
way to automatically iterate over those elements.

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      shopping_list_items = ['apples', 'oranges', 'bananas', 'bread', 'toothpaste']

      print('You need to buy:')
      for item in shopping_list_items:     # Iterate by element
         print('\t' + item)
      
   **Console Output**

   ::

      You need to buy:
         apples
         oranges
         bananas
         bread
         toothpaste

The syntax almost reads like natural language: *For each item in
shopping_list_items, print a tab character plus the item*.

Each time the loop repeats, Python assigns the next element in the list to the
loop variable ``item``. The elements may be of any data type.

.. admonition:: Tip

   To keep the meaning of your code clear, use plural names for your
   lists---like ``fruits``, ``cars``, ``even_numbers``, etc.

   When you iterate through a list, use the singular name for the loop
   variable.

   #. ``for fruit in fruits:``
   #. ``for car in cars:``
   #. ``for even_number in even_numbers:``

   This helps you explain what your code is doing. For example, in step 2, you
   can think to yourself, *Each time the loop repeats, my code takes one
   car element from the cars list*.

Loop by Index
-------------

We can also use the ``range`` command to generate index values, and then use
bracket notation to access each element from the list:

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      shopping_list_items = ['apples', 'oranges', 'bananas', 'bread', 'toothpaste']

      for index in range(len(shopping_list_items)):     # Iterate by index
         print("{0}) {1}".format(index+1, shopping_list_items[index]))
      
   **Console Output**

   ::

      1) apples
      2) oranges
      3) bananas
      4) bread
      5) toothpaste

For this loop, ``range(len(shopping_list_items))`` generates a sequence of
integers (0, 1, 2...) up to but not including the length of the list.

Each time the loop repeats, Python assigns the next integer in the sequence to
the loop variable ``index``.

In line 4, note how we use the ``index`` values to calculate the item numbers
and access each element from the list.

"Do Something With" vs. "Do Something To"
-----------------------------------------

.. todo:: Not happy with the flow of the writing in this section. Ideas?

Should we *iterate by element* or *iterate by index*? In many cases, the choice
comes down to personal preference. Sometimes, however, one option will be
better than the other.

The following example shows a case where we do something WITH the list
elements:

.. admonition:: Example

   Given ``scores = [10, 25, 8, 33, 0]``, the code shows two ways to add up all
   of the values from the list:

   .. sourcecode:: Python
      :linenos:

      for score in scores:             # Option 1: Loop by element
         total_points += score
      
      for index in range(len(scores)): # Option 2: Loop by index
         total_points += scores[index]

The end result is the same for both loops, ``total_points`` winds up with a
value of ``76``. However, the syntax for looping by element (option 1) is
cleaner, since we do not have to worry about bracket notation.

This example shows doing something WITH the list elements. We access each one
in turn and add it to ``total_points``. We do NOT change any of the elements
themselves. ``print(scores)`` returns ``[10, 25, 8, 33, 0]`` even after the
loop finishes.

The next example shows a case where we do something TO the list elements:

.. admonition:: Example

   Given ``scores = [10, 25, 8, 33, 0]``, the code below adds extra points to
   some of the values:

   .. sourcecode:: Python
      :linenos:
      
      print(scores)

      for index in range(len(scores)):    # Loop by index
         if index >= 2:                   # Check position in list
            scores[index] += 12           # Increase the value of the element

      print(scores)

   **Console Output**

   ::

      [10, 25, 8, 33, 0]
      [10, 25, 20, 45, 12]
   
   Take a moment to think about what happens inside the loop. We must keep
   track of both the *location* of an element in the list and its *value*.
   
   #. We do NOT add more points if the element's value is larger than 2.
   #. Instead, we add more points if the *location* of the element in the list
      is at index 2 or later.

Since lists are mutable, we can use a loop to change some or all of the
elements. To do this, we must know the *position* of the element in the list,
and this requires an index value.

Take Home Idea
^^^^^^^^^^^^^^

#. If we just need to access the values inside a list without changing them,
   iterating by element is the cleaner approach. Looping by element also avoids
   *index out of range* errors. (*Doing something WITH the list values*)
#. If we need to change one or more of the values in a list, then we MUST loop
   by index. (*Doing Something TO the list values*)
#. Doing something with only certain list elements??????

Try It!
-------

The following program contains a list of turtle colors and shapes. It is an
extension of the sprite loop, but the idea here is to use the number of colors
in the list to draw and shade each leg.

.. raw:: html

   <iframe height="800px" width="100%" src="https://repl.it/@launchcode/LCHS-Turtle-Lists?lite=true" scrolling="no" frameborder="yes" allowtransparency="true" allowfullscreen="true"></iframe>

#. On line 15, set up a ``for`` statement that iterates through the elements in
   the ``colors`` list.

   a. Inside the loop, use the loop variable to set the color for ``bob``.
   b. Move ``bob`` forward and back 75 units. (If you wish, add a stamp at the
      end of each leg).
   c. Use ``bob.left(360/len(colors))`` to make ``bob`` rotate by the proper
      amount.
   d. Run your program to verify that your code works (feel free to change the
      number of elements in the ``colors`` list). Properly done, your output
      should behave something like this:

      .. figure:: figures/color-sprite.gif
         :alt: Gif showing a turtle drawing a six-sided sprite with each leg a different color.

#. On line 12, set up a ``for`` statement that iterates by index through the
   ``colors`` list.
   
   a. Inside the loop, use the ``index`` value to reassign the color values in
      the list.
   b. Replace each string in the list with the darker version of the same
      color (e.g. ``blue`` gets replaced with ``dark blue``).
   c. Run your program to verify that your code works. Properly done, your
      output should now behave something like this:

      .. figure:: figures/dark-color-sprite.gif
         :alt: Gif showing a turtle drawing a six-sided sprite with each leg a new color.

#. *BONUS*: Using index values, try iterating over both the ``shapes`` and
   ``colors`` lists.

      .. figure:: figures/shape-color-sprite.gif
         :alt: Gif showing a six-sided sprite drawn with different turtle colors and shapes.
