Checking Strings
================

It is often helpful to examine a character and test whether it is upper- or
lowercase, or whether it is a character or a digit.

We can use bracket notation and string methods inside a boolean expression to
check if a string meets a certain condition.

.. todo:: Insert internal book link to the boolean expression section.

Checking Type
-------------

The string methods only work on string objects. For ``my_var = 'Python'``,
``my_var.upper()`` works just fine. However, if we were to reassign a number
to the variable, like ``my_var = 3.14159``, then ``my_var.upper()`` throws an
error.

Let's see how we can use the ``type()`` function to check for a string.

.. admonition:: Example

   .. todo:: Insert interactive repl here! (Check variable type).

   .. sourcecode:: Python
      :linenos:

      my_var = 42

      if type(my_var) == str:
         print("The value '{0}' is a string.".format(my_var))
      else:
         print("The value {0} is NOT a string.".format(my_var))

   Run the program with each of the following values for ``my_var``:

   #. '1234' vs. 1234
   #. ``True`` or ``False`` vs. ``"True"`` or ``"False"``
   #. 0.3333 vs. '0.333'
      
We can easily modify line 3 to check if ``my_var`` is an ``int``, ``float``,
or ``bool`` data type. We could also use an ``if/elif/else`` block to check for
the different data types.  (*TRY IT*!)

.. admonition:: Note

   We could avoid the conditional block completely with:

   .. sourcecode:: Python

      print("The value {0} is a {1} data type.".format(my_var, type(my_var))

   but that defeats the purpose of the example---*checking the data type*.    

Comparing Strings
-----------------

We can use the comparison operators ``==, !=, <, >, <=, >=`` on strings.

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      my_pet = 'dog'
      your_pet = 'cat'
      other_pet = 'crow'

      print(my_pet == your_pet)
      print(your_pet[0] == other_pet[0])
      print(my_pet < your_pet)
   
   **Console Output**

   ::

      False
      True
      False

#. Line 5 evaluates if the strings ``'dog'`` and ``'cat'`` are identical and
   then prints the boolean result (``False``).
#. Line 6 evaluates if the first character in ``'cat'`` and ``'crow'`` are the
   same (``True``).

   - Note that the first character comparison for ``'cat'`` and ``'Crow'``
     would return ``False`` due to the different cases.
   - To make the expression *case-insensitive*, we need to convert each
     character to the same case (e.g.
     ``your_pet[0].lower() == other_pet[0].lower()``).

#. Line 7 evaluates if ``'dog'`` comes earlier in the alphabet than ``'cat'``.
   A string that comes earlier is considered *less than* a string that comes
   later. Since ``'dog'`` follows ``'cat'`` alphabetically, the expression
   ``'dog' < 'cat'`` evaluates to ``False``.
   
.. admonition:: Note

   Case matters when alphabetizing! By convention, we consider CAPITAL letters
   to come EARLIER in the alphabet than lowercase letters.
   
   ``'Zebra' < 'apple'`` is ``True``, but ``'zebra' < 'apple'`` is ``False``.

Checking with ``in`` and ``not in``
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If we want to find out if a certain character is in a string, we could iterate
through the string and compare each character to the one we want.

.. sourcecode:: Python
   :linenos:

   title = 'The Hunger Games'
   search_character = 'e'

   for char in title:
      if char == search_character:
         print("'{0}' is in '{1}'.".format(search_character, title))

However, this is inefficient, since the loop continues even after we find
``search_character``. As coded, the program prints the output once each time
``search_character`` is found.

A better approach is to use the ``in`` operator (or its opposite, ``not in``)
to return the same information. The ``in`` operator tests if one string is a
substring of another.

.. sourcecode:: Python
   :linenos:

   title = 'The Hunger Games'
   search_character = 'e'

   if search_character in title:
      print("'{0}' is in '{1}'.".format(search_character, title))

.. admonition:: Try It!

   Use the ``in`` (or ``not in``) operator to count the number of vowels in a
   string.

   .. todo:: Insert interactive repl here (in vs. not in).

   .. sourcecode:: Python
      :linenos:

      text = "Armadillos or anteaters"
      vowels = 'aeiou'
      vowel_count = 0

      for char in text:
         if char in vowels:
            count += 1
      
      print(f"'{text}' contains {vowel_count} vowels.")

   #. The program does not quite work yet. There are 9 vowels in
      ``'Armadillos or anteaters'``, but the code does not count the capital
      ``A``.
   #. Fix the code to be *case-insensitive*. Both capital and lowercase vowels
      should increase ``vowel_count``.
   #. Modify the code to give the number of consonants (non-vowels) in the
      string.

Checking Case
-------------

The ``upper()`` and ``lower()`` methods return a new string with all of the
letters shifted to the same case. Recall, however, that the methods do NOT
change the original string. This gives us a way to check the case for either a
single character, a slice, or the entire string.

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      title = "Harry Potter and the Sorcerer's Stone"
      cap_count = 0

      for char in title:
         if char.upper() == char:
            cap_count += 1

      print(f"'{title]' contains {cap_count} capital letters.")
      
      if title.upper() == title:
         print("Stop yelling!")
      elif title.lower() == title:
         print("The title is not capitalized correctly.")

   In line 5, ``char.upper()`` creates a new string (the uppercase version of
   ``char``) and compares it to the original. If they match, then the original
   character in ``title`` is a capital letter, and ``cap_count`` gets increased
   by 1.

   In a similar manner, lines 10 and 12 check if the entire string is either
   all uppercase or all lowercase.

Check Your Understanding
------------------------ 

Evaluate whether the following expressions are ``True`` or ``False``:

.. admonition:: Question

   .. sourcecode:: Python

      "dog" < "doghouse"

   .. raw:: html
   
      <ol type="a">
         <li><input type="radio" name="Q1" autocomplete="off" onclick="evaluateMC(name, true)"> <span style="color:#419f6a; font-weight: bold">True</span></li>
         <li><input type="radio" name="Q1" autocomplete="off" onclick="evaluateMC(name, false)"> <span style="color:#419f6a; font-weight: bold">False</span></li>
      </ol>
      <p id="Q1"></p>

.. Answer = True

.. admonition:: Question

   .. sourcecode:: Python

      "dog" < "Dog"

   .. raw:: html
   
      <ol type="a">
         <li><input type="radio" name="Q2" autocomplete="off" onclick="evaluateMC(name, false)"> <span style="color:#419f6a; font-weight: bold">True</span></li>
         <li><input type="radio" name="Q2" autocomplete="off" onclick="evaluateMC(name, true)"> <span style="color:#419f6a; font-weight: bold">False</span></li>
      </ol>
      <p id="Q2"></p>

.. Answer = False

.. admonition:: Question

   .. sourcecode:: Python

      "dog" < "Doghouse"
   
   .. raw:: html
   
      <ol type="a">
         <li><input type="radio" name="Q3" autocomplete="off" onclick="evaluateMC(name, false)"> <span style="color:#419f6a; font-weight: bold">True</span></li>
         <li><input type="radio" name="Q3" autocomplete="off" onclick="evaluateMC(name, true)"> <span style="color:#419f6a; font-weight: bold">False</span></li>
      </ol>
      <p id="Q3"></p>

.. Answer = False

.. admonition:: Question

   .. sourcecode:: Python

      "app" in "Happy"

   .. raw:: html
   
      <ol type="a">
         <li><input type="radio" name="Q4" autocomplete="off" onclick="evaluateMC(name, true)"> <span style="color:#419f6a; font-weight: bold">True</span></li>
         <li><input type="radio" name="Q4" autocomplete="off" onclick="evaluateMC(name, false)"> <span style="color:#419f6a; font-weight: bold">False</span></li>
      </ol>
      <p id="Q4"></p>

.. Answer = True 

.. admonition:: Question

   For which of the following would ``text.upper() == text`` return
   ``True``?

   .. raw:: html
   
      <ol type="a">
         <li><input type="radio" name="Q5" autocomplete="off" onclick="evaluateMC(name, false)"> <span style="color:#419f6a; font-weight: bold">text = 'Stop Yelling!'</span></li>
         <li><input type="radio" name="Q5" autocomplete="off" onclick="evaluateMC(name, true)"> <span style="color:#419f6a; font-weight: bold">text = 'STOP YELLING!'</span></li>
         <li><input type="radio" name="Q5" autocomplete="off" onclick="evaluateMC(name, false)"> <span style="color:#419f6a; font-weight: bold">text = 'stop yelling!'</span></li>
         <li><input type="radio" name="Q5" autocomplete="off" onclick="evaluateMC(name, false)"> <span style="color:#419f6a; font-weight: bold">text = 'STOP YELLINg!'</span></li>
         <li><input type="radio" name="Q5" autocomplete="off" onclick="evaluateMC(name, false)"> All return <span style="color:#419f6a; font-weight: bold">True</span></li>
         <li><input type="radio" name="Q5" autocomplete="off" onclick="evaluateMC(name, false)"> None return <span style="color:#419f6a; font-weight: bold">True</span></li>
      </ol>
      <p id="Q5"></p>

.. Answer = b

.. raw:: html

   <script type="text/JavaScript">
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
