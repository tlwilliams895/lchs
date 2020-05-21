Lists Are Like Strings
======================

Besides being ordered collections, Python lists show other similarities to
strings.

List Length
-----------

.. index::
   single: list; length

Just like strings, the ``len()`` function returns the length of a list (the
number of elements in the list).

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      letters = ['a', 'b', 'c', 'x', 'y', 'z']

      print("The list {0} has {1} elements.".format(letters, len(letters))
   
   **Console Output**

   ::

      The list ['a', 'b', 'c', 'x', 'y', 'z'] has 6 elements.

   In line 3, ``len(letters)`` returns the number of items stored in the
   ``letters`` list.

.. admonition:: Note

   We will explore how the ``len()`` function deals with nested lists (like
   ``[['a', 'b', 'c'], ['x', 'y', 'z']]``) later in this chapter.

Note that the statement ``print(letters[len(letters)])`` will throw an *index
out of range* error. Since index values start at 0, the last element in any
list will always have a value of ``len(list_name) - 1``.

``in`` and ``not in``
---------------------

Just like strings, we can use the ``in`` and ``not in`` operators to check if a
specific value is present in a list. The operators return ``True`` or ``False``
depending on if the value matches an element.

.. _in-not-in-editor:

.. admonition:: Try It!

   Run this program to see the results returned by the ``in`` and ``not in``
   operators.

   .. raw:: html

      <iframe height="500px" width="100%" src="https://repl.it/@launchcode/LCHS-in-and-not-in-List-Example?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true"></iframe>

   Note that even though the substring ``'nana'`` is present in ``'banana'``,
   the result of line 5 is still ``False``. In this case, the ``in`` operator
   checks if the string ``'nana'`` is its own element in ``fruit``. To check if
   ``'nana'`` is a smaller piece of each element requires more code.

List Slices
-----------

.. index::
   single: list; slice

Just like strings, we can return a *slice* (several elements) from a list.
Taking a slice creates a new list, and the syntax should be familiar:

.. sourcecode:: Python

   list_name[start_index : end_index]

The new list contains the elements from ``start_index`` up to but NOT including
``end_index``. If we leave out ``start_index``, the slice starts at the
beginning of the list. If we leave out ``end_index``, the slice continues to
the end of the list.

The index values in the new list begin at 0.

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      original_list = [2, 4, 6, 8, 10, 12, 14]
      
      new_list = original_list[2:5]

      print(new_list, 'vs.', original_list)
      print(new_list[0])
      print(original_list[:3])
      print(original_list[3:])

   **Console Output**

   ::

      [6, 8, 10] vs. [2, 4, 6, 8, 10, 12, 14]
      6
      [2, 4, 6]
      [8, 10, 12, 14]

Try It!
^^^^^^^

In the :ref:`editor above <in-not-in-editor>`, add slices to check only a
portion of the ``fruit`` list (e.g. ``print("apple" in fruit[2:4])``).

Check Your Understanding
------------------------

.. admonition:: Question

   What is printed by the following code?

   .. sourcecode:: Python
      :linenos:

      a_list = [4, 2, 8, 6, 5, 4]
      a_list[2] = True
      print(a_list)

   .. raw:: html

      <ol type="a">
         <li><input type="radio" name="Q1" autocomplete="off" onclick="evaluateMC(name, false)"> [4, 2, True, 8, 6, 5, 4]</li>
         <li><input type="radio" name="Q1" autocomplete="off" onclick="evaluateMC(name, false)"> [4, True, 2, 8, 6, 5, 4]</li>
         <li><input type="radio" name="Q1" autocomplete="off" onclick="evaluateMC(name, true)"> [4, 2, True, 6, 5, 4]</li>
         <li><input type="radio" name="Q1" autocomplete="off" onclick="evaluateMC(name, false)"> [4, True, 8, 6, 5, 4]</li>
      </ol>
      <p id="Q1"></p>

.. Answer = c

.. admonition:: Question

   Given ``num_list = [8, 6, 7, 5, 3, 0, 9]``, what does ``num_list[2:5]``
   return?

   .. raw:: html

      <ol type="a">
         <li><input type="radio" name="Q2" autocomplete="off" onclick="evaluateMC(name, true)"> [7, 5, 3]</li>
         <li><input type="radio" name="Q2" autocomplete="off" onclick="evaluateMC(name, false)"> [7, 5, 3, 0]</li>
         <li><input type="radio" name="Q2" autocomplete="off" onclick="evaluateMC(name, false)"> [6, 7, 5]</li>
         <li><input type="radio" name="Q2" autocomplete="off" onclick="evaluateMC(name, false)"> [6, 7, 5, 3]</li>
      </ol>
      <p id="Q2"></p>

.. Answer = a

.. admonition:: Question

   Given ``fruit = ["apple", "orange", "banana", "cherry", "tomato", "bell pepper"]``,
   which of the following statements return ``True``? Select ALL that apply.

   .. raw:: html
      
      <ol type="a">
         <li><span id = "a" onclick="highlight('a', false)">apples in fruit</span></li>
         <li><span id = "b" onclick="highlight('b', false)">pepper in fruit</span></li>
         <li><span id = "c" onclick="highlight('c', true)">banana in fruit[:3]</span></li>
         <li><span id = "d" onclick="highlight('d', false)">tomato in fruit[1:4]</span></li>
         <li><span id = "e" onclick="highlight('e', true)">broccoli not in fruit</span></li>
         <li><span id = "f" onclick="highlight('f', true)">orange not in fruit[2:]</span></li>
      </ol>

.. Answers = c, e, f

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
