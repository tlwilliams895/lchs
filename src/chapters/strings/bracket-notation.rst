Bracket Notation
================

.. index:: 
   single: string; index

.. index:: ! index

Strings are *ordered* collections of characters, and this gives us a nice
mental model for how they are put together. Each character has its own specific
location within a string, and we call this location the **index**.

Consider the string ``'Go Python!'`` The first character, ``'G'``, has an index
value of 0, the first ``'o'`` has index 1, the space ``' '`` has index 2, and
so on. Index values are integers representing the position of a character
within a given string.

.. figure:: ./figures/index-figure.png
   :alt: The string "Go Python!" with index values labeled below each character.

   The index values of a string.

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

The expression ``'school'[2]`` selects the character at index ``2`` and creates
a new string containing just this one character.

With zero-based indexing, the letter at index 0 of ``'school'`` is ``'s'``. So
at position [2] we have the letter ``'h'``.

.. admonition:: Try It!

   Predict which letters will be printed to the console. Check your answers by
   clicking *Run*. Remember that with zero-based indexing, the *first*
   character always has an index value of ``0``.

   .. raw:: html

      <iframe height="400px" width="100%" src="https://repl.it/@launchcode/LCHS-Bracket-Practice-Strings?lite=true" scrolling="no" frameborder="yes" allowtransparency="true"></iframe>

   Now try the following:

   #. Change the index values in lines 3 and 5 to see how they affect the
      output.
   #. Enter ``40`` into the brackets in line 3. What happens when you use an
      index value that is larger than the length of the string?
   #. Replace ``40`` inside the brackets with a negative number, like ``-1``.
      What happens?

In step 2 above, ``this_string[40]`` causes an *index out of range* error.
This happens anytime we try to reference an index location that does not exist
in the string.

Expressions for ``index``
^^^^^^^^^^^^^^^^^^^^^^^^^

If we want to access the *last* character in a string, we need to know its
index value. How can we find this number without having to count all of the
characters first?

An index value must either be an integer---like 0, 1, 2, etc.---or an
expression that evaluates to an integer.

Recall that we can use the ``len()`` function to return the number of
characters in a string.

.. sourcecode:: Python
   :linenos:

   this_string = 'Zero-based indexing!'

   print(len(this_string))

**Console Output**

::

   20

In the *Try It* example above, replace ``print(this_string[3])`` with
``print(this_string[len(this_string)])``.

Wait...what? We got an *index out of range* error, but we KNOW that
``this_string`` is 20 characters long!

The reason is, once again, zero-based indexing. Since we start counting the
index values at ``0``, the 20th character has an index value of ``19``.

.. admonition:: Tip

   We can access the last character of the string and avoid the out of range error
   by using:

   .. sourcecode:: python

      print(this_string[len(this_string) - 1])

   The expression ``len(this_string) - 1`` evaluates to ``19``, and
   ``this_string[19]`` is the last character (``'!'``).

Negative Index Values
---------------------

Lorem ipsum...

Check Your Understanding
------------------------

.. admonition:: Question

   If ``phrase = 'Code for fun'``, then ``phrase[2]`` evaluates to:

   #. ``"o"``
   #. ``"d"``
   #. ``"for"``
   #. ``"fun"``

.. admonition:: Question

   Which of the following returns ``true`` given ``myStr = 'Index'``?  Choose all correct answers.

   #. ``myStr[2] === 'n';``
   #. ``myStr[4] === 'x';``
   #. ``myStr[6] === ' ';``
   #. ``myStr[0] === 'I';``

.. admonition:: Question

   What is printed by the following code?

   .. sourcecode:: js
      :linenos:

      let phrase = "JavaScript rocks!";
      console.log(phrase[phrase.length - 8]);

   #. ``"p"``
   #. ``"i"``
   #. ``"r"``
   #. ``"t"``

.. admonition:: Question

   Given ``language = 'Python``, what does ``language[1,4]`` return?

   #. ``"Pyth"``
   #. ``"Pyt"``
   #. ``"yth"``
   #. ``"ytho"``

.. Answer: d

.. raw:: html

   <script type="text/JavaScript">
      function highlight(id, answer) {
         text = document.getElementById(id).innerHTML
         if (answer) {
            document.getElementById(id).style.background = 'lightgreen';
            document.getElementById(id).innerHTML = text + ' - Correct!';
         } else {
            document.getElementById(id).innerHTML = text + ' - Nope!';
            document.getElementById(id).style.color = 'red';
         }
      }

      function evaluateMC(id, correct) {
         if (correct) {
            document.getElementById(id).innerHTML = 'Yep!';
            document.getElementById(id).style.color = 'blue';
         } else {
            document.getElementById(id).innerHTML = 'Nope!';
            document.getElementById(id).style.color = 'red';
         }
      }
   </script>
