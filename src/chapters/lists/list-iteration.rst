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

When should we *iterate by element* or *iterate by index*? In most cases, both
methods accomplish the same thing. However, there is a small difference in how
each method uses the list items.

The following example shows a case where we do something WITH the list
elements:

.. admonition:: Example

   Given ``scores = [10, 25, 8, 33, 0]``, the code below shows two ways to use
   a loop to add up all of the values from the list:

   .. sourcecode:: Python
      :linenos:

      for score in scores:             # Option 1: Loop by element
         total_points += score
      
      for index in range(len(scores)): # Option 2: Loop by index
         total_points += scores[index]



Since lists are mutable, we can use a loop to modify each element. The
following code squares all the numbers from 1 to 5 using iteration by position.

Turtle Lists
------------

[IDEA: Iterate through a list of turtles to make each move and/or to assign
properties. (Starburst pattern?)]
