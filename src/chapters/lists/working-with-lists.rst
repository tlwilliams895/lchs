Working with Lists
==================

.. index:: ! mutable

Unlike strings, lists are **mutable**. This means we can change the values of
the elements inside the list, add new elements to the list, remove items from
the list, or change the order of the elements.

Changing One Element
--------------------

To update a single item in a list, use the syntax:

.. sourcecode:: python

   list_name[index] = new_value

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      grocery_list = ["granola bars", "veggies", "TP", "other healthy stuff"]
      print(grocery_list)

      grocery_list[0] = "pears"
      grocery_list[-1] = "chocolate"
      print(grocery_list)

   **Console Output**

   ::

      ['granola bars', 'veggies', 'TP', 'other healthy stuff']
      ['pears', 'veggies', 'TP', 'chocolate']

Removing Elements (Part 1)
--------------------------

To remove one or more elements from a list, we can use the ``del`` function.
Here, ``del`` stands for *delete*.

The general syntax is:

.. sourcecode:: python

   del list_name[index]       # Removes the element at index.
   del list_name[start:end]   # Removes the elements from 'start' up to but NOT
                              # including 'end'.

Note that ``del`` does NOT use parentheses ``()``.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      num_strings = ['one', 'two', 'three']
      del num_strings[1]      # Removes the element at index 1.
      print(num_strings)

      letter_list = ['a', 'b', 'c', 'x', 'y', 'z']
      del letter_list[1:5]    # Removes each element from index 1 - 4.
      print(letter_list)

   **Console Output**

   ::

      ['one', 'three']
      ['a', 'z']

There are multiple ways to add or remove elements from a list. We will examine
these below and on the :ref:`List Methods <list-methods>` page.

The Slice Operator
------------------

Used on the *right hand side* of the ``=`` operator, a slice returns a smaller
portion of a list.

::

   new_list = old_list[start : end]

Used on the *left hand side* of the ``=`` operator, a slice will either
*insert, replace, or remove* elements.

The general syntax is:

::

   list_name[start : end] = [new values...]

Note that the new values must be inside brackets ``[]`` and separated from each
other by commas.

Inserting New Elements
^^^^^^^^^^^^^^^^^^^^^^

Make the ``start`` and ``end`` values the same. This inserts all of the new
values into the list, starting at the chosen index. Existing elements get
pushed to later positions in the list.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      my_list = [3, 6, 9, 12]
      print(my_list)

      my_list[2:2] = ['a', 'b', 'cde'] # Inserts 3 new elements starting at index 2.
      print(my_list)

   **Console Output**

   ::

      [3, 6, 9, 12]
      [3, 6, 'a', 'b', 'cde', 9, 12]

Replacing Elements
^^^^^^^^^^^^^^^^^^

Make the ``start`` and ``end`` values different. The elements from index
``start`` to ``end`` (NOT including ``end``) get replaced with the new values.

Note that the number of old and new values can be different.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      my_list = [10, 20, 30, 40, 50, 60, 70, 80]
      print(my_list)

      my_list[1:6] = [-1, -3] # Replaces the elements from indexes 1 - 5 with two new values.
      print(my_list)

   **Console Output**

   ::

      [10, 20, 30, 40, 50, 60, 70, 80]
      [10, -1, -3, 70, 80]

Removing Elements (Part 2)
^^^^^^^^^^^^^^^^^^^^^^^^^^

The syntax is the same as above, but use the empty list instead of specific
values.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      my_list = [10, 20, 30, 40, 50, 60, 70, 80]
      print(my_list)

      my_list[1:6] = [] # Removes the elements from indexes 1 - 5.
      print(my_list)

   **Console Output**

   ::

      [10, 20, 30, 40, 50, 60, 70, 80]
      [10, 70, 80]

Combining Lists
---------------

We can combine lists to create a new, longer list.

.. admonition:: Try It!

   Experiment with using different operators on two lists. Keep notes about the
   results.

   #. Can we add two lists?  Try printing ``one_list + another_list``.
   #. Can we subtract two lists? Try printing ``one_list - another_list``.
   #. Multiplication? Kinda. Try printing ``one_list * 3``.

   .. todo:: Insert interactive repl here (list concatenation)!

Try It!
-------

.. admonition:: Example

   In the editor below:

   #. Change a single value inside ``my_list``.
   #. Use ``del`` to remove a single value from ``my_list``.
   #. Use ``del`` to remove multiple values from ``my_list``.
   #. Practice using the slice operator to insert, remove, or replace one or
      more elements from ``my_list``.
   
   .. todo:: Insert interactive repl here (mutating lists)!

Check Your Understanding
------------------------

Lorem ipsum...
