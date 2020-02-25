.. _booleans:

Boolean Values and Boolean Expressions
======================================

.. index:: data type

One of the key features of *any* programming language is the ability to decide
whether to run a segment of code. This means you can make your code run a set
of statements *only if* a given condition is met.

.. admonition:: Example

   Consider an application that reminds you when you have an overdue book. The
   app sends you a message *only if* the due date has passed and you have not
   returned the book.

The *condition* for this example depends on the status of the book. If the
condition is true (overdue), a message gets sent.

In order to have Python make this type of decision, we need to understand how
programming languages represent *true* and *false*.

Boolean Values
--------------

.. index:: ! True, ! False, ! boolean

.. index::
   single: boolean; value

You have already explored the data types ``string``, ``int``, and ``float``.
The Python data type for storing true and false values is called ``boolean``
(named after the British mathematician George Boole).

.. admonition:: Fun Fact

   George Boole created `Boolean Algebra <https://en.wikipedia.org/wiki/Boolean_algebra>`__,
   which is the basis of all modern computer arithmetic.

There are only two **boolean values**---``True`` and ``False``. Since Python is
case-sensitive, ``true`` and ``false`` are *not* valid boolean values.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      print(True, False)
      print(type(True))
      print(type(False))

   **Console Output**

   ::

      True False
      <class 'bool'>
      <class 'bool'>

The values ``True`` and ``False`` are *not* strings. If you use quotes to
surround booleans (``"True"`` and ``"False"``), those values become strings.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      print(type(True))
      print(type("True"))

   **Console Output**

   ::

      <class 'bool'>
      <class 'str'>

Boolean Expressions
-------------------

.. index::
   single: boolean; expression

.. index::
   single: operator; equality

.. index:: ! ==

A **boolean expression** is an expression that evaluates to either ``True`` or
``False``. The equality operator, ``==``, compares two values and returns true
or false depending on whether the values are equal.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      num = 37
      other_num = 38

      print(5 == 5)
      print(15 == 16)
      print(num == other_num)

   **Console Output**

   ::

      True
      False

In line 4, the two values are equal, so the expression evaluates to ``True``.
In the line 5, 15 is not equal to 16, so we get ``False``. Line 7 shows that we
can compare the values stored in one or more variables.

We can also use ``==`` to see that ``True`` and ``"True"`` are NOT equal.

.. admonition:: Example

   .. sourcecode:: python

      print(True == "True")

   **Console Output**

   ::

      False

Comparison Operators
^^^^^^^^^^^^^^^^^^^^

.. index::
   single: operator; comparison

The ``==`` operator is one of six common **comparison operators**.

.. index:: ==, ! !=, ! <, ! >, ! <=, ! >=

.. list-table:: Comparison Operators
   :widths: auto
   :header-rows: 1

   * - Operator
     - Description
     - Examples Returning ``True``
     - Examples Returning ``False``
   * - Equal (``==``)
     - Returns ``True`` if two compared values are equal, and ``False`` otherwise.
     - ``7 == 7``

       ``"dog" == "dog"``
     - ``7 == 5``

       ``"dog" == "cat"``
       ``cat`` == ``Cat``
   * - Not equal (``!=``)
     - Returns ``True`` if two compared values are NOT equal, and ``False`` otherwise.
     - ``7 != 5``

       ``"dog" != "cat"``
     - ``7 != 7``

       ``"dog" != "dog"``
   * - Greater than (``>``)
     - Returns ``True`` if the left-hand value is greater than the right-hand value, and ``False`` otherwise.
     - ``7 > 5``

       ``'b' > 'a'``
     - ``5 > 7``

       ``'a' > 'b'``
   * - Less than (``<``)
     - Returns ``True`` if the left-hand value is less than the right-hand value, and ``False`` otherwise.
     - ``5 < 7``

       ``'a' < 'b'``
     - ``7 < 5``

       ``'b' < 'a'``
   * - Greater than or equal (``>=``)
     - Returns ``True`` if the left-hand value is greater than or equal to the right-hand value, and ``False`` otherwise.
     - ``7 >= 5``

       ``7 >= 7``

       ``'b' >= 'a'``

       ``'b' >= 'b'``
     - ``5 >= 7``

       ``'a' >= 'b'``
   * - Less than or equal (``<=``)
     - Returns ``True`` if the left-hand value is less than or equal to the right-hand value, and ``False`` otherwise.
     - ``5 <= 7``

       ``5 <= 5``

       ``'a' <= 'b'``

       ``'a' <= 'a'``
     - ``7 <= 5``

       ``'b' <= 'a'``

Although these operations are probably familiar, the Python symbols differ
slightly from the mathematical symbols.

A common error is to use a single equals sign (``=``) instead of a double
equals (``==``) when comparing two values. Remember that ``=`` is an
*assignment* operator and ``==`` is a *comparison* operator.

#. To set or change the value of a variable, use ``=`` (e.g. ``name = 'Mae'``).
#. To compare two different values, use ``==`` (e.g. ``name == other_name``).

An equality test is *symmetric*, meaning that we can swap the places of the
operands and the result is the same.  For a variable ``a``, if ``a == 7`` is
``true`` then ``7 == a`` is also ``true``. However, an assignment statement is
not symmetric: ``a = 7`` is legal while ``7 = a`` is not.

Check Your Understanding
------------------------

.. admonition:: Question

   Which of the following is a Boolean expression? Select all that apply.

   #. ``3 == 4``
   #. ``3 + 4``
   #. ``3 + 4 === 7``
   #. ``"false"``

