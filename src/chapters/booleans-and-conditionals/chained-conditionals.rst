Chained vs. Sequential Conditionals
===================================

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

As with a simple ``if`` statement, the ``else`` clause is optional in this
context as well. The following example does not print anything, since both
conditions evaluate to false and there is no ``else`` clause.

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
