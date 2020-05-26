Lists Within Lists
==================

Earlier we learned that lists can store values of any data type. Does this mean
we can store lists inside of lists? Well, yes we can...

.. index:: ! multi-dimensional list, ! nested list

.. index::
   single: list; nested

A **multi-dimensional list** is a list of lists, meaning that the values inside
the list are also lists.

A **nested list** is a list that appears as an element inside another list.
Nested lists can store strings, numbers, and even more lists.

.. sourcecode:: python

   multidim_list = ['a', 'b', [1, 2, 3], 'rutabaga']

In ``multidim_list``, the element at index 2 is a nested list. If we
``print(multidim_list[2])``, we see ``[1, 2, 3]`` appear in the console.

The figure below demonstrates a ``synonyms`` list that has lists as values. The
*nested* lists contain words that are synonyms of each other. Notice each inner
list has an index position.  

.. todo:: Insert figure for a multi-dimensional list here!

   A label, synonyms, pointing to a list that contains lists at it's four
   indexes. Each inner list has a list of words that are synonyms. 

Two Dimensional Lists
---------------------

The simplest form of a multi-dimensional list is a two dimensional list. Each
element is a nested list, which contains multiple data values.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      two_dim_list = [['a', 'b', 'c'], [90, 101], [True, False, False, True]]

      print(len(two_dim_list))

   **Console Output**

   ::

      3

``two_dim_list`` holds three elements, each of which is a list. Note that the
``len()`` function only counts these three elements and NOT the total number of
items inside of these nested lists.

To access items in a two dimensional list, use two sets of square brackets and
two index values. The indexes evaluate from left to right. The first index
selects one of the nested lists, and the second index selects an element from
that nested list.

.. admonition:: Example

   Use a two dimensional list to contain three different lists of space shuttle
   crews.

   .. sourcecode:: python
      :linenos:

      two_dim_list = [['a', 'b', 'c'], [90, 101], [True, False, False, True]]

      print(two_dim_list[0])
      print(two_dim_list[1])
      print(two_dim_list[2])

      print(two_dim_list[0][2])
      print(two_dim_list[1][1])
      print(two_dim_list[2][3])

   **Console Output**

   ::
      ['a', 'b', 'c']
      [90, 101]
      [True, False, False, True]

      c
      101
      True

Multi-Dimensions and List Methods
----------------------------------

In a multi-dimensional list, both the inner and outer lists can be altered
with list methods. However, bracket notation must be used correctly.

To apply a method to the outer list, the syntax is:

.. sourcecode:: python

   multilist_name.method()

To apply a method to one of the inner lists, the syntax is:

.. sourcecode:: python

   multilist_name[index_of_nested_list].method()

.. admonition:: Example

   Use list methods to add an additional crew list and alter existing lists.

   .. sourcecode:: python
      :linenos:

      shuttle_crews = [
         ['Robert Gibson', 'Mark Lee', 'Mae Jemison'],
         ['Kent Rominger', 'Ellen Ochoa', 'Bernard Harris'],
         ['Eilen Collins', 'Winston Scott',  'Catherin Coleman']
      ]

      let newCrew = ['Mark Polansky', 'Robert Curbeam', 'Joan Higginbotham']

      # Add a new crew list to the end of shuttleCrews
      shuttleCrews.push(newCrew)
      print(shuttleCrews[3][2])

      # Reverse the order of the crew at index 1
      shuttleCrews[1].reverse()
      print(shuttleCrews[1])

   **Console Output**

   ::

      Joan Higginbotham
      [ 'Bernard Harris', 'Ellen Ochoa', 'Kent Rominger' ]

Beyond Two Dimensional lists
-----------------------------

Generally, there is no limit to how many dimensions you can have when creating
lists. However it is rare that you will use more than two dimensions. Later on
in the class we will learn about more collection types that can handle complex
problems beyond the scope of two dimensional lists.


Check Your Understanding
------------------------

.. admonition:: Question

   What are the two dimensional indexes for ``"Jones"``?

   .. sourcecode:: python
      :linenos:

      school = [
         ["science", "computer", "art"],
         ["Jones", "Willoughby", "Rhodes"]
      ]



   How would you add ``"dance"`` to the list at ``school[0]``?

   How would you add ``"Holmes"`` to the list at ``school[1]``?

