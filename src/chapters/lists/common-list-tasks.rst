Common List Tasks
=================

Lorem ipsum...

Accumulating List Elements
--------------------------

Just like strings, we can use the accumulator pattern to add items to a list.

.. admonition:: Example

   Let's begin by adding even numbers to an empty list:

   .. sourcecode:: python
      :linenos:

      evens = []     # evens is the accumulator variable

      for num in range(0, 21, 2):  # num takes the values 0, 2, 4...20.
         evens.append(num)         # Add the value of num to the end of the list.

      print(evens)

   **Console Output**

   ::

      [0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

   Now let's add selected elements from one list to another:

   .. sourcecode:: python
      :linenos:

      words = ['It', 'was', 'a', 'bright', 'cold', 'night', 'in', 'April', 'and', 'all', 'the', 'clocks', 'were', 'striking', 'thirteen']   
      a_words = []        # Accumulator list

      for word in words:            # word takes the value of each element from words.
         if word[0].lower() == 'a': # True if word starts with 'a' or 'A'.
            a_words.append(word)    # Add word to the list.

      print(a_words)

   **Console Output**

   ::

      ['a', 'April', 'and', 'all']

.. admonition:: Note

   One benefit of using the accumulator pattern is that it preserves the
   original list.

Adding To Multiple Lists
^^^^^^^^^^^^^^^^^^^^^^^^

In the same accumulator loop, we can use a conditional to decide which list
receives a value.

.. admonition:: Example

   Let's divide a list of mixed data types:

   .. sourcecode:: python
      :linenos:

      mixed_types = [5, 7, 3.14, 'rutabaga', 'integer', True]
      integers = []
      strings = []

      for item in mixed_types:
         if type(item) == str:
            strings.append(item)
         elif type(item) == int:
            integers.append(item)
      
      print(mixed_types)
      print(integers)
      print(strings)
   
   **Console Output**

   ::

      [5, 7, 3.14, 'rutabaga', 'integer', True]
      [5, 7]
      ['rutabaga', 'integer']

   Note that the values ``3.14`` and ``True`` are not placed into either
   list, since they are of the ``float`` and ``bool`` data types,
   respectively.

We could easily extend the ``if/elif`` block to deal with other data types.

.. admonition:: Try It!

   .. todo:: Insert interactive repl here (list accumulation).

   Add statements to the code to assign elements from the ``strings`` list
   into either ``vowel_start``, ``digit_start``, or ``other_start``.

   .. sourcecode:: python
      :linenos:

      strings = ['apple', 'banana', '9-to-5', '@launchcode', 'everyone can code', ':-)', '4EVR']
      vowel_start = []
      digit_start = []
      other_start = []

      for item in strings:
         if item[0].lower() in 'aeiou':
            vowel_start.append(item)
         elif item[0] in '0123456789':
            digit_start.append(item)
         else:
            other_start.append(item)

   **Expected Output**

   ::

      ['apple', 'everyone can code']
      ['9-to-5', '4EVR']
      ['banana', '@launchcode', ':-)']

Finding Max and Min
-------------------

Often, we want to find the largest or smallest value from the elements in a
list. We can accomplish this two different ways.

.. admonition:: Example

   Sorting a list arranges the elements from the smallest to largest value.
   The maximum (or minimum) value can then be accessed with bracket notation.

   .. sourcecode:: python
      :linenos:

      numbers = [42, 27, 30, 46, -36, 30, -28, 53, 53, 32]
      output = "Minimum = {0}, Maximum = {1}"

      numbers.sort()
      print(numbers)
      print(output.format(numbers[0], numbers[-1]))
      # Index 0 is the first element in the list, and index -1 is the last.

   **Console Output**

   ::

      [-36, -28, 27, 30, 30, 32, 42, 46, 53, 53]
      Minimum = -36, Maximum = 53

.. admonition:: Example

   Python also has two functions, ``max()`` and ``min()``, that return the
   largest and smallest values from a collection.

   .. sourcecode:: python
      :linenos:

      numbers = [42, 27, 30, 46, -36, 30, -28, 53, 53, 32]
      output = "Minimum = {0}, Maximum = {1}"

      largest = max(numbers)
      smallest = min(numbers)
      print(numbers)
      print(output.format(smallest, largest))

   **Console Output**

   ::

      [42, 27, 30, 46, -36, 30, -28, 53, 53, 32]
      Minimum = -36, Maximum = 53

   Since the ``max`` and ``min`` functions *return* a value, we could easily
   use the expressions inside ``format``.

   .. sourcecode:: python
      :lineno-start: 4

      print(numbers)
      print(output.format(min(numbers), max(numbers)))

.. admonition:: Note

   Finding the maximum and minimum values also works with strings.

   ``max(['apple', 'bear', 'zebra', 'display'])`` returns ``'zebra'``, and
   ``min('telescope')`` returns ``'c'``.

Check Your Understanding
------------------------

Lorem ipsum...
