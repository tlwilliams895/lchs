Truth Tables
============

.. index:: ! truth table

**Truth tables** help us understand how logical operators work by showing all
of the possible return values. Let's look at the truth table for ``and``, which
assumes we have two boolean expressions, ``A`` and ``B``.

.. admonition:: Example

   .. list-table:: Truth Table for ``and``
      :widths: auto
      :header-rows: 1

      * - A
        - B
        - A ``and`` B
      * - ``True``
        - ``True``
        - ``True``
      * - ``True``
        - ``False``
        - ``False``
      * - ``False``
        - ``True``
        - ``False``
      * - ``False``
        - ``False``
        - ``False``

Consider the first row of the table. This row states that if A is true
and B is true, then A and B is true. The two middle rows show that if
either A or B is false, then A and B is false. Finally, if both A and B are
false, then A and B is false.

Order of Operations
-------------------

.. index:: order of operations

We now have a number of operators in our toolkit. It is important to understand
how these operators relate to each other. Which ones get done first?

Python always performs operations in a specific order:

#. Complete all math calculations
#. Evaluate all comparisons as ``True`` or ``False``
#. Apply all ``not`` operators
#. Evaluate ``and`` and ``or`` operations

This means that the expression ``x * 5 >= 10 && y - 6 <= 20`` will be evaluated
so as to first perform the arithmetic and then check the relationships. The
``&&`` evaluation will be done last. The order of evaluation is the same as if
we were to use parentheses to group, as follows:

.. sourcecode:: js

   ((x * 5) >= 10) && ((y - 6) <= 20)

While parentheses are not always necessary due to default operator precedence,
they make expressions much more readable. As a best practice, we encourage you
to use them, especially for more complicated expressions.

The following table lists operators in order of precedence, from highest (applied first) to lowest (applied last). A complete table for the entire language can be found in the `MDN Python Documentation <https://developer.mozilla.org/en-US/docs/Web/Python/Reference/Operators/Operator_Precedence#Table>`_.

.. list-table:: Operator Precedence
   :widths: auto
   :header-rows: 1

   * - Precedence
     - Category
     - Operators
   * - (highest)
     - Logical NOT
     - ``!``
   * -
     - Exponentiation
     - ``**``
   * -
     - Multiplication and division
     - ``*``, ``/``, ``%``
   * -
     - Addition and subtraction
     - ``+``, ``-``
   * -
     - Comparison
     - ``<=``, ``>=``, ``>``, ``<``
   * -
     - Equality
     - ``===``, ``!==``, ``==``, ``!=``
   * -
     - Logical AND
     - ``&&``
   * - (lowest)
     - Logical OR
     - ``||``

Check Your Understanding
------------------------

.. admonition:: Question

   Complete the table below.

   .. list-table:: Truth Table for ``or``
      :widths: auto
      :header-rows: 1

      * - A
        - B
        - A ``or`` B
      * - ``True``
        - ``True``
        -
      * - ``True``
        - ``False``
        -
      * - ``False``
        - ``True``
        -
      * - ``False``
        - ``False``
        -
