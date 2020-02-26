Logical Operators
=================

.. index:: operators

Recall that an *operator* carries out an action on one or more operands
(values). In the Data and Variables chapter we learned about the different
math operators (``+``, ``-``, ``*``, ``/``, ``//``. ``**``, and ``%``), which
we use to perform calculations.

   TODO: Add chapter link!

We also saw how the operators ``+`` and ``*`` behave when applied to strings,
and we practiced with compound assignment operators, such as ``+=`` and ``-=``.

Boolean Operators
-----------------

.. index::
   single: operator; comparison
   single: operator; boolean
   single: operator; logical

In the previous section, we learned about comparison operators like ``==`` and
``<``. These operators are part of a larger class known as
**boolean operators**, so-called because they each return a value of either
``True`` or ``False``.

Three additional boolean operators allow us to make more complex comparisons.
These are called **logical operators**, and there are only three---``and``,
``or``, and ``not``.

``n - 2 == 0 or n - 3 == 0`` is true if EITHER of the conditions is true. In
this case, only one part has to be true for the overall result to be true.

Logical ``and``
^^^^^^^^^^^^^^^

.. index:: ! and

.. index::
   single: boolean; expression, compound

Here is one boolean expression: ``num > 0``. It returns ``True`` when ``num``
has any value larger than 0.

Another boolean expression is ``num < 10``, which returns ``True`` when ``num``
has any value smaller than 10.

A **compound boolean expression** is a boolean expression built out of smaller
ones. Python allows us to combine expressions by using the ``and`` operator.

.. sourcecode:: Python

   num > 0 and num < 10

Here, ``num > 0 and num < 10`` is true only if ``num`` is greater than 0 AND,
at the same time, ``num`` is less than 10. The compound expression returns only
ONE boolean value, which depends on the results from BOTH of the smaller
comparisons.

Stated again: Logical ``and`` combines two operands, and the resulting
expression is ``True`` only if *both* operands return ``True``. If either
operand is ``False``, the overall expression is ``False``.

.. admonition:: Example

   The meaning of ``and`` resembles its use in English. A sentence like "Roses
   are red and violets are blue," is true as a whole precisely because roses are
   actually red, and violets are actually blue.

   On the other hand, the sentence "Roses are red and violets are green," is
   false as a whole. While roses are indeed red, violets are NOT green.

Let's see how this works in Python code.

.. admonition:: Example

   .. sourcecode:: Python
      :linenos:

      num = 5
      print(num > 0 and num < 10)

      print(7 > num and num == 3)

      print(num*5 > 100 and 'dog' == 'cat')

   **Console Output**

   ::

      True
      False
      False

In line 2, ``num > 0 and num < 10`` evaluates to ``True`` because both
``num > 0`` and ``num < 10`` are ``True`` individually.

In line 4, the expression ``7 > num and num == 5`` evaluates to ``False``
because one of the two comparisons, ``num == 3``, is ``False``.

Line 6, evaluates to ``False`` because both comparisons return ``False``.
Notice that we can mix and match data types however we like, as long as both
sides of the ``and`` expression are themselves boolean expressions.

Logical ``or``
^^^^^^^^^^^^^^

.. index:: ! or

Python's logical ``or`` also combines two boolean expressions. In this case,
however, the resulting expression is ``True`` if *either* of the operands are
``True`` individually. If both operands are ``False``, the overall expression
is ``False``.

.. admonition:: Example

   Logical ``or`` also resembles our English experience. The sentence "Pigs can
   fly, or dogs can run," is true as a whole. Even though pigs cannot fly, dogs
   CAN run. Only one of the two statements has to be true in order for the whole
   sentence to be true.

   When both of the statements joined by "or" are false, the statement as a
   whole is false. "Pigs can fly or the Earth is flat," is a false statement.

Let's look at some more code examples.

.. sourcecode:: Python
   :linenos:

   num = 5
   print(num > 0 or num < 10)

   print(7 > num or num == 3)

   print(num*5 > 100 or 'dog' == 'cat')

**Console Output**

::

   True
   True
   False

Lines 2 and 4 both return ``True`` because at least one of the comparisons
joined by ``or`` is ``True``. Line 6 returns ``False`` because both of the
comparisons are ``False``.

Logical ``not``
^^^^^^^^^^^^^^^

.. index:: ! not

The logical ``not`` operator takes a single operand and flips its boolean
value. If a comparison evaluates to ``False``, then applying ``not`` changes
the result to ``True`` (and vice versa).

.. admonition:: Examples

   .. sourcecode:: python
      :linenos:

      print(not True)
      print(not False)

      num = 5

      print( not(num < 7) )
      print( not('dog' == 'cat') )
      print( not(num*5 > 100 or 'dog' == 'cat') )

   **Console Output**

   ::

      False
      True
      False
      True
      True

Longer Combinations
-------------------

In the examples above, we used the ``and`` and ``or`` operators to combine two
smaller boolean expressions. However, we can use the operators to combine as
many comparisons as we want!

.. sourcecode:: Python
   :linenos:

   num = 5
   python = 'Awesome!'

   print(num > 0 and num < 10 and 'dog' == 'cat')
   print(num > 7 or num == 3 or 'dog' == 'cat' or python == 'Awesome!')

**Console Output**

::

   False
   True

.. admonition:: Warning

   Here is a VERY common mistake programmers make when they try to combine
   boolean expressions.

   What if we have a variable ``num`` and we want to check if its value is 5, 6,
   or 7?

   #. If we try to describe this out loud, we might say, “num is equal to 5 or 6
      or 7”.
   #. If we translate this into Python as ``num == 5 or 6 or 7``,
      we get an error when we run the code.

   To prevent this error, we must combine three separate equality comparisons,
   ``num == 5 or num == 6 or num == 7``. This may seem like a lot of typing but
   it is necessary.

Check Your Understanding
------------------------

.. admonition:: Question

   What is returned by the following boolean expression?

   .. sourcecode:: python

      4 < 3 or 2 < 3

   #. ``True``
   #. ``False``
   #. ``"True"``
   #. ``"False"``

.. Answer = a

   TODO: Add more CC questions.
