Taking a Slice
==============

.. index:: ! substring, ! slice

In addition to accessing single characters in a string, we can also use bracket
notation to access multiple characters. This smaller set of characters is
called a **substring** of the original.

A substring is also called a **slice** of the original string. Selecting a
slice is similar to selecting a character, and the syntax is:

.. sourcecode:: Python

   some_string[start_index : end_index]

With this format, Python returns all of the characters from the ``start_index``
value up to but NOT including the ``end_index`` value.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      alphabet = 'abcdefghijklmnopqrstuvwxyz'
      substring = alphabet[2:5]

      print(substring)

   **Console Output**

   ::

      cde

   Since we start counting at 0, the character at index value 2 is ``'c'``,
   and the character at index 5 is ``'f'``. However, note that ``'f'`` is
   NOT included in the slice.

If we leave out the first index (before the colon), the slice starts at the
beginning of the string. If we leave out the second index, the slice goes to
the end of the string.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      fruit = "cucumber"
      print(fruit[:3])
      print(fruit[3:])

   **Console Output**

   ::

      cuc
      umber
   
   What do you think ``fruit[:]`` means?

Saving Substrings
^^^^^^^^^^^^^^^^^

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
