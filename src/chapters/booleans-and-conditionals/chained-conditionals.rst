Chained Conditionals
====================

A **chained conditional** consists of a series of checks that are evaluated one
after the other. If a check in the series evaluates to ``True``, then all of
the following checks are ignored.

``elif`` Statements
----------------------

.. index:: conditional, ! elif

If-else statements provide two alternative paths. A single condition determines
which path to follow. We can build more complex conditionals using an
**elif** clause. ``elif`` stands for *else if*, and it allows us to add more
conditions and code blocks to our conditionals. This leads to more branches for
our code to follow.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      num = 10
      other_num = 20

      if num > other_num:
         print(num, "is greater than", other_num)
      elif num < other_num:
         print(num, "is less than", other_num)
      else:
         print(num, "is equal to", other_num)

   **Console Output**

   ::

      10 is less than 20

**Summary:**

#. Line 4 begins the conditional. The boolean expression ``num > other_num``
   returns ``False``, since 10 is not greater than 20. This causes line 5 to be
   skipped.
#. Line 6 contains the ``elif`` statement. The boolean expression
   ``num < other_num`` returns ``True``, since 10 is less than 20. This
   triggers line 7.
#. The code block for the ``else`` clause (line 9) is skipped, because one of
   the conditions above was true.

.. admonition:: Note

   Just like with a simple ``if`` statement, the ``else`` clause is optional for
   ``elif`` statements as well. In the example above, removing lines 8 & 9 will
   not break anything. However, the program will not print anything when
   ``num`` equals ``other_num``, since the ``if`` and ``elif`` conditions are
   both ``False``.

Word Analysis Redo
^^^^^^^^^^^^^^^^^^

On the previous page, we used a nested conditional to print different outputs
based on the length of a word. We can accomplish the same result with a
chained conditional.

.. admonition:: Example

   Here is the nested conditional again:

   .. sourcecode:: python
      :linenos:

      word = input('Please enter a word: ')

      if len(word) == 4:
         print("What did your mom tell you about using 4-letter words?")
      else:
         if len(word) < 4:
            print("You can think of a longer word than that!")
         else:
            print("Excellent word!")

   The following chained conditional produces the same result:

   .. sourcecode:: python
      :linenos:

      word = input('Please enter a word: ')

      if len(word) == 4:
         print("What did your mom tell you about using 4-letter words?")
      elif len(word) < 4:
         print("You can think of a longer word than that!")
      else:
         print("Excellent word!")

Nested vs. Chained
^^^^^^^^^^^^^^^^^^

Nesting one conditional inside of another performs a *check within a check*,
and we can do this any number of times.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      if condition_1:
         # code here

         if condition_2:
            # code here

            if condition_3:
               # code here
            else:
               # code here

         else:
            # code here

      else:
         # code here

Perhaps you see the problem with nesting more than once or twice. The code
quickly gets very difficult to read and follow.

Even though we COULD code a check within a check within a check within a check
within a check (etc.), we really SHOULDN'T. In most instances, we can
make our code more readable by using chained conditionals and/or logical
operators in place of nested conditionals.

Next Section
------------



.. sourcecode:: python
   :linenos:

   let x = 10;
   let y = 10;

   if (x > y) {
       console.log("x is greater than y");
   } else if (x < y) {
       console.log("x is less than y");
   }

We can construct conditionals using ``if``, ``else if``, and ``else`` with a
lot of flexibility. The only rules are:

#. We may not use ``else`` or ``else if`` without a preceding ``if``
   statement.
#. ``else`` and ``else if`` clauses are optional.
#. Multiple ``else if`` statements may follow the ``if`` statement, but they
   must precede the ``else`` clause, if one is present.
#. Only one ``else`` clause may be used.

Regardless of the complexity of a conditional, *no more than one* of the code
blocks will be executed.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      let x = 10;
      let y = 20;

      if (x > y) {
         console.log("x is greater than y");
      } else if (x < y) {
         console.log("x is less than y");
      } else if (x % 5 === 0) {
         console.log("x is divisible by 5");
      } else if (x % 2 === 0) {
         console.log("x is even");
      }

   **Console Output**

   ::

      x is less than y

Even though both of the conditions ``x % 5 == 0`` and ``x % 2 == 0`` evaluate
to ``True``, neither of the associated code blocks is executed. When a
condition is satisfied, the rest of the conditional is skipped.

Check Your Understanding
------------------------

.. admonition:: Question

   What does the following code print?

   .. sourcecode:: python
      :linenos:

      a = 8

      if a % 2 == 0:
         print("Launch")
      elif a > 5:
         print("Code")
      else:
         print("LaunchCode")

   #. ``"Launch"``
   #. ``"Code"``
   #. ``"Launch"``

      ``"Code"``
   #. ``"LaunchCode"``
