Exercises: Booleans and Conditionals
====================================

If your teacher has added to you a *repl.it classroom*, complete the exercises
there. Otherwise, follow the links to *standard repl.it* (no auto-grader).

Part A: Basic Selection
-----------------------

   Repl.it link goes here!

``if`` Only
^^^^^^^^^^^

Prompt the user to enter a word and store the result in ``user_entry``:

.. sourcecode:: python

   user_entry = input('Enter a word: ')

#. Use a conditional to check the length of the word. If longer than 5
   characters, print, ``"___ is longer than 5 characters."`` Otherwise, print
   nothing. (Note: Fill in the blank with the value of ``user_entry``).

Binary Selection
^^^^^^^^^^^^^^^^

Prompt the user to enter a number:

.. sourcecode:: python

   num_entry = input('Enter a number larger than 100: ')

2. Check if ``num_entry`` is 100 or larger. If so, print, ``"Valid entry!"``
   Else print, ``"Number too small."``
#. Check if ``user_entry`` is all lowercase. If so, print, ``"___ is all
   lowercase."`` Else, print, ``"___ is NOT all lowercase."`` Fill in the blank
   with the value of ``user_entry``. (*Hint*: Take advantage of the
   ``.lower()`` string method).

The ``in`` keyword can be used as another comparison operator.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      print('ana' in 'banana')
      print('z' in 'apple')

   **Console Output**

   ::

      True
      False

   The string ``ana`` is present within ``banana``, while there is no
   ``z`` character within ``apple``.

4. Use the ``in`` operator to check if ``user_entry`` starts with a vowel. If
   so, print, ``"___ starts with a vowel."`` Else, print, ``"___ does NOT start
   with a vowel."``

Part B: Logical Operators
-------------------------

   Repl.it link goes here!

Lorem ipsum...

Part C: Chained Conditionals
----------------------------

Lorem ipsum...

Part D: Nested Conditionals
---------------------------

Lorem ipsum...
