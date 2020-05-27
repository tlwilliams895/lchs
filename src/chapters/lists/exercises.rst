Exercises: Lists
================

The following actions will teach you how to add, remove, modify and
rearrange list elements.

.. todo:: Add admonition for using repl.it classroom vs. standard repl.it!

Part One: Adding and Removing Items
-----------------------------------

.. todo:: Add repl.it link for list exercises, part 1.

#. Create a list called ``adding_practice`` with a single entry: ``273.15``.
   Use the ``append`` method to add the following elements to the list one at a
   time. Print the list after each step to confirm the changes.

   #. 42
   #. "hello"

#. Use :ref:`concatenation <concatenating-lists>` to add these three items to
   the list all at once: ``[False, -4.6, '87']``.

   *Congratulations!. You can now add items to a list.*

#. ``append``, ``insert``, ``pop``, and ``remove`` are used to add or remove
   elements from a list. *Bracket notation* can be used to modify any element
   within a list. Starting with the ``cargo_hold`` list

   ::

      ['oxygen tanks', 'space suits', 'parrot', 'instruction manual', 'meal packs', 'slinky', 'security blanket']
   
   write statements to do the following:

   #. Use bracket notation to replace ``'slinky'`` in the list with ``'space
      tether'``. Print the list to confirm the change.
   #. Remove the last item from the list with ``pop``. Print the element
      removed and the updated list.
   #. Remove the first item from the list with ``pop``. Print the element
      removed and the updated list.
   #. ``append`` and ``insert`` require arguments inside the ``()``. Add the
      items 1138 and ‘20 meters’ to the the list---the number at the start and
      the string at the end. Print the updated list to confirm the changes.
   #. ``remove`` the parrot from the cargo hold, then print the updated list.
   #. Use ``format()`` to print the final contents of the list and its length.
      ``"The list ___ contains ___ items."``

   *Status check: Where do ``append`` and ``insert`` add new items to a list?
   What is the difference between ``pop`` and ``remove``? Which methods require
   entries inside the ``()``?*

Part Two: Slices & Methods
--------------------------

.. todo:: Add repl.it link for list exercises, part 2.

#. Using the slice syntax ``list_name[start : end]`` you can either insert,
   replace, or remove items from a list. Review the
   :ref:`List Slices <slicing-lists>` section if you need a syntax reminder.

   Use slices to make the following changes to the final ``cargo_hold`` list
   from part 1. Be sure to print the list after each step to confirm your
   work.

   #. Insert the string ``'keys'`` at index 3 without replacing any other
      entries.
   #. Remove 'instruction manual' from the list. (Hint: The ``index`` method is
      helpful to avoid manually counting an index).
   #. Replace the elements at indexes 2 - 4 with the items ``'cat'``,
      ``'fob'``, and ``'string cheese'``.

   *Well done, cadet. Now let's look at some finer details about list methods.
   We've got to keep our paperwork straight, so you need to know when your
   actions change the original records.*

#. Some methods---like ``append`` and ``pop``---alter the original list,
   while others do not. Use the lists

   .. sourcecode:: python

      supplies_1 = ['duct tape', 'gum', 3.14, False, 6.022e23]
      supplies_2 = ['orange drink', 'nerf toys', 'camera', '42', 'Rutabaga']

   to see if taking a slice or using the ``reverse`` and ``sort`` methods
   changes the original list.

   #. Print a slice of the last 3 items from ``hold_cabinet_1``. Does slice
      alter the original list? Verify this by printing ``hold_cabinet_1``
      after taking the slice.
   #. ``reverse`` the first list, ``sort`` the second, and then print both
      lists. What is the difference between the two methods?
   #. Do reverse or sort alter the original lists?

   *Good progress, cadet. Here are two more methods for you to examine.*

Part Three: Split, List, and Join
---------------------------------

.. todo:: Add repl.it link for list exercises, part 3.

#. The ``split`` method converts a string into a list, while the ``join``
   method does the opposite.

   #. Try it! Given the string ``phrase = 'In space, no one can hear you code.'``,
      see what happens when you print ``phrase.split()`` vs.
      ``phrase.split('e')`` vs. ``list(phrase)``. What is the purpose of the
      argument inside the ``()``?
   #. Given the list ``my_list = ['B', 'n', 'n', 5]``, see what happens when
      you print ``''.join(my_list)`` vs. ``'a'.join(my_list)`` vs.
      ``'_'.join(my_list)``. What is the purpose of the argument inside the
      ``()``?
   #. We can take a string with *delimiters* (like commas) and convert it into
      a modifiable list. Try it! Split the string
      ``"water,space suits,food,plasma sword,batteries'`` at each comma,
      alphabetize the list with ``sort``, then combine the elements into a new
      string. Use a hyphen to join the elements together in the string.
   #. Do ``split`` or ``join`` change the original string/list?

   *Nicely done, astronaut. Now it's time to bring you fully up to speed.*

Part Four: Multi-dimensional Lists
----------------------------------

.. todo:: Add repl.it link for list exercises, part 4.

#. lists can hold different data types, even other lists! A
   *multi-dimensional list* is one with entries that are themselves lists.

   #. Define and initialize the following lists, which hold the name, chemical
      symbol and mass for different elements:

      i. ``element_1 = ['hydrogen', 'H', 1.008]``
      ii. ``element_2 = ['helium', 'He', 4.003]``
      iii. ``element_26 = ['iron', 'Fe', 55.85]``

   #. Define the list ``table``, and use ``append(list_name)`` to add each of
      of the element lists to it. Print ``table`` to see its structure.
   #. Use bracket notation to examine the difference between printing
      ``table[1]`` and ``table[1][1]``. Don't just nod your head! I want to
      HEAR you describe this difference. Go ahead, talk to your screen.
   #. Using bracket notation and the ``table`` list, print the mass of
      element_1, the name for element_2 and the symbol for element_26.
   #. ``table`` is an example of a *2-dimensional list*. The first "level"
      contains the element lists, and the second level holds the
      name/symbol/mass values. **Experiment!** Create a 3-dimensional list and
      print out one entry from each level in the list.

*Excellent work, records keeper. Welcome aboard.*
