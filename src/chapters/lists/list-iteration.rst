Iterating Through Lists
=======================

Just like with strings, we can use a loop to iterate through the elements in a
list.

Iterate by Element
------------------

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

Each iteration, Python assigns the next element in the list to the loop
variable ``item``. The elements may be of any data type.

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

Iterate by Index
----------------

Lorem ipsum...

"Do Something With" vs. "Do Something To"
-----------------------------------------

Lorem ipsum...

Turtle Lists
------------

[IDEA: Iterate through a list of turtles to make each move and/or to assign
properties. (Starburst pattern?)]
