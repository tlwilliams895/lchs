Other Operators
===============

Earlier, you learned how to assign, then *reassign* a variable:

.. sourcecode:: python
   :linenos:

   day = "Thursday"
   print(day)
   day = "Friday"
   print(day)

**Console Output**

::

   Thursday
   Friday

One of the most common forms of this involves making the new value of the
variable depend on the old value.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      my_number = 10
      print(my_number)
      my_number = my_number + 2
      print(my_number)

   **Console Output**

   ::

      10
      12

The new value of ``my_number`` equals its old value plus 2.

Updating Variables
------------------

The statement ``my_number = my_number + 2`` tells Python, take the current
value of ``my_number``, increase it by ``2``, then reassign the result to
``my_number``.

This type of update is so common in Python (and programming in general) that we
have an operator to use as a shortcut.

.. sourcecode:: python
   :linenos:

   my_number = my_number + 2
   my_number += 2

Lines 1 and 2 do exactly the same thing. The operator ``+=`` increases the
value of ``my_number`` by 2.

In general, ``+=`` increases the value of a first operand by the amount of the
second operand.

.. index:: ! compound assignment operator

``+=`` is an example of a **compound assignment operator**, or an operator that
performs two actions in the same statement---a calculation and an assignment.

.. list-table:: Compound Assignment Operators
   :widths: auto
   :header-rows: 1

   * - Operator
     - Meaning
   * - ``a += b``
     - ``a = a + b``
   * - ``a -= b``
     - ``a = a - b``
   * - ``a *= b``
     - ``a = a * b``
   * - ``a /= b``
     - ``a = a / b``

The String Operator ``+``
--------------------------

.. index::
   pair: string; concatenation

So far we have only seen operators that work on operands which are numbers, but
there are operators that work on other data types as well. In particular, the
``+`` operator can be used with ``string`` operands to join them together.

.. admonition:: Example

   ``"Launch" + "Code"`` evaluates to ``"LaunchCode"``

Let's compare ``+`` used with numbers to ``+`` used with strings.

Try It!
^^^^^^^

   INSERT REPL HERE...

This example demonstrates that the ``+`` operator *behaves differently based on
the data type of its operands.*

.. admonition:: Warning 

   So far we have only seen examples of operators working with data of like
   type. For the examples ``1 + 1`` and ``"1" + "1"``, both operands are of
   type ``int`` and ``str``, respectively.

   It is possible, however, to mix types with an expression such as
   ``1 + "1"``. The results of doing so can be unexpected, and at this stage
   of your coding journey we strongly advise against creating such expressions.

   We will explore such "mixed" operations in a later chapter.
