Bracket Notation
================

.. index:: 
   single: string; index

.. index:: ! index

Strings are *ordered* collections of characters, and this gives us a nice
mental model for how they are put together. Each character has its own specific
location within a string, and we call this location the **index**.

Consider the string ``'Go Python!'``. The first character, ``'G'``, has an
index value of 0, the first ``'o'`` has index 1, the space ``' '`` has index 2,
and so on. Index values are integers representing the position of a character
within a given string.

.. figure:: ./figures/index-figure.png
   :alt: The string "Go Python!" with index values labeled below each character.

.. index:: zero-based indexing

Note that this is another example of *zero-based indexing*. The count begins
with the value 0.

Access One Character
--------------------

.. index:: ! bracket notation

**Bracket notation** is the special syntax that allows us to access the single
characters that make up a string. To access a character, we use the syntax:

.. sourcecode:: Python

   some_string[index]

where ``index`` is the position of the character we want.

The expression ``some_string[2]`` gives the character at index ``2``.

.. admonition:: Try It!

   Predict which letters will be printed to the console. Check your answers by
   clicking *Run*.

   .. todo:: Enter bracket notation repl here!!!

   .. sourcecode:: Python
      :linenos:

      this_string = 'Zero-based indexing!'
      
      print(this_string[3])

      print("Alphabet soup'[5])
   
   Recall that with zero-based indexing, the *first* character always has an
   index value of ``0``.

   Try the following:

   #. Change the index values in lines 3 and 5 to see how they affect the
      output.
   #. What happens if you use an index that doesn't exist, like a number larger
      than the length of the string? TRY IT! Enter ``20`` into the brackets in
      line 3.
   #. Place a negative number, like ``-1``, inside the brackets. What happens?

Saving Characters
^^^^^^^^^^^^^^^^^

Lorem ipsum...

Negative Index Values
^^^^^^^^^^^^^^^^^^^^^

Lorem ipsum...

Taking a ``slice``
------------------

Lorem ipsum...
