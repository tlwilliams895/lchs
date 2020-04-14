Loop Through a String
=====================

The ``range`` command assigns the loop variable a new integer value each time
the loop repeats. What if we want to assign the variable something *other* than
whole numbers?

Characters Instead of Integers
------------------------------

Recall that a string is a series of characters enclosed in quotes, like
``'Hello, World!'`` or ``"Python"``. Just like ``range`` assigns a new integer
to the loop variable, we can set up a ``for`` loop to assign different
characters from a string.

Run the following program to see how this works:

.. raw:: html

   <iframe height="500px" width="100%" src="https://repl.it/@launchcode/LCHS-Loop-Through-A-String?lite=true" scrolling="no" frameborder="yes"></iframe>

Some points to notice:

#. In the ``for`` statement, a string (or a variable containing a string)
   replaces ``range``.
#. The first time the loop runs, the loop variable gets assigned the first
   character in the string (``character = 'H'`` or ``char = 'T'``).
#. Each time the loop repeats, the variable stores next character in the
   string.
#. Unlike ``range(n)``, which does NOT assign the value of ``n`` to the loop
   variable, the last character in the string IS used.
#. Once Python reaches the end of the string, the loop ends.

Characters Another Way
----------------------

Take a look at the following code and its output:

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      word = 'Python'

      print(word)
      print(word[0])
      print(word[1])
      print(word[5])
   
   **Console Output**

   ::

      Python
      P
      y
      n

Notice how lines 4 - 6 each print a single character from the string. Instead
of displaying the entire string, ``word[0]`` produces the first letter, ``P``.
``word[1]`` gives us the second character, and ``word[5]`` gives us the last.

We will explore strings in more detail in a later chapter. For now, we just
need to recognize that every character in a string has an *index*. An index
is a number that tells us the location of a character in the string.

Just like ``range``, the index values of a string begin counting at ``0``.

   INSERT DIAGRAM HERE.

Indexes provide a different way to loop through a string:

   INSERT REPL HERE!!!!

.. sourcecode:: Python
   :linenos:

   word = 'Python'

   for index in range(6):
      print(word[index])

Some items to note:

#. By using ``range``, the ``index`` variable will take values from 0 - 5.
#. ``word[index]`` refers to the character in the string at position ``index``.
#. As written, the loop only displays characters up to index 5. TRY IT---Replace
   the string with a longer one.
#. If we replace the string with a shorter one, we get an error! For
   ``word[5]`` to work, there must be a character at index 5.
#. To prevent "index out of range" errors in this loop, we should NOT use
   a specific number inside ``range``. TRY IT---Replace ``range(6)`` with
   ``range(len(word))``. ``len(word)`` always returns the length of the current
   string, so changing that string will not break the loop.

Check Your Understanding
------------------------

Lorem ipsum...
