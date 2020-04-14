The Accumulator Pattern
=======================

.. index:: algorithm, ! pattern

Recall that an *algorithm* is a set of specific steps that, when followed,
solve a problem.

A **pattern** is similar to an algorithm, but it can be used to solve many
different types of problems. Think of a *pattern* like tying a knot---you can
use the same steps to tie your shoelaces, a drawstring, the handles of a
plastic bag, the ribbon on a present, etc. The pattern is the act of tying, and
it is part of a larger solution (e.g. cleaning up after your dog). Often, a
pattern makes up part of a larger algorithm.

Even though two algorithms can solve very different problems, the same pattern
might be found in each one.

Let's take a look at your first coding pattern.

Keeping a Running Total
-----------------------

Assume you are working at a theater, and your job is to keep track of how many
people walk through the front door. To help you keep track of the total, your
boss gives you a counting tool. Every time a person walks in, you push a button
and *CLICK*, the total displayed on the tool increases by 1.

.. index:: ! accumulator pattern

This is an example of the **accumulator pattern**. Every time a particular
event occurs, the value of a running total gets updated.

In programming, the accumulator pattern occurs VERY often. The key pieces to
this pattern include:

#. A variable that starts at some basic value. For numbers, this value is
   usually ``0`` or ``1``. For the ``str`` data type, begin with the empty
   string, ``""`` or ``''``.
#. A loop.
#. Inside the loop, the value of the variable steadily increases (or decreases)
   with each iteration.

Let's look at some code to see how the accumulator pattern works.

Adding ``1...num``
^^^^^^^^^^^^^^^^^^

Let's write a program that adds up the numbers from 1 to ``num``, where
``num`` stores some integer.

If we did this with pencil and paper, finding the sum might look like this
when ``num = 6``:

::

   (1 + 2) + 3 + 4 + 5 + 6   # Calculate 1 + 2
   (3 + 3) + 4 + 5 + 6       # Calculate 3 + 3
   (6 + 4) + 5 + 6           # Calculate 6 + 4
   (10 + 5) + 6              # Calculate 10 + 5
   (15 + 6)                  # Calculate 15 + 6
   21                        # Final result!

In each step, the *running total* is the first number, and it gets added to the
next value in the series. As we move down the steps, we see the total increase
from 1 to 3 to 6 etc.

For larger values of ``num``, solving this process by hand gets tedious really
fast. Loops to the rescue!

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      num = 6
      total = 0

      for integer in range(1, num+1):
         total += integer

      print(total)

   **Console Output**

   ::

      21

#. In line 2, we assign a value of ``0`` to the variable ``total``.
#. Each time the loop body runs, the loop variable ``integer`` is assigned a
   new, higher value (1 to 6).

   .. admonition:: Note

      Recall that with ``range(start, end)``, the loop variable takes each value
      from ``start`` up to but NOT including ``end``. This is why line 4 uses
      ``range(1, num+1)``. We want to include the value of ``num`` as part of the
      iteration.

#. Each time line 5 runs, the current value of ``integer`` is added to
   ``total``.
#. Once the loop ends, ``total`` contains the sum of all the individual values.

The loop carries out the same basic algorithm that we used to compute the sum
``1 + 2 + 3 + 4 + 5 + 6`` by hand. When we do this on paper, we usually do not
write down a running total for simple steps like 1 + 2. With programming,
however, we must store this total in a variable.

.. index:: ! accumulator

.. index::
   single: pattern, accumulator

The variable ``total``` is called the **accumulator**, which is a fancy way of
saying that it gathers up all the individual integers one by one.

.. admonition:: Tip

   The key to using the accumulator pattern successfully is to initialize the
   accumulator variable *before* you start the loop. Once inside the loop,
   update the variable.

Building a String
^^^^^^^^^^^^^^^^^

Let's write a program that builds a new string using the accumulator pattern.
For this example, the new string will be a copy of a larger one, but it will
contain only vowels.

   INSERT REPL HERE!!!

#. On line 2, define a variable called ``only_vowels`` and assign it the empty
   string, ``''``. This will be the *accumulator*, and it will get larger as
   the loop runs.
#. On line 4, set up a ``for`` statement to loop through the characters in
   ``some_text``.

   .. sourcecode:: python

      for char in some_text:

#. Inside the loop, we want to check if ``char`` is a vowel. If ``True``, add
   ``char`` to ``only_vowels``. If ``False``, we will not update
   ``only_vowels``. Paste this code into the loop. Remember to indent!

   .. sourcecode:: python
      :lineno-start: 5

      if char in 'aeiou':     # Check if char is a vowel.
         only_vowels += char  # If True, add char to only_vowels.
      
      print(only_vowels)

#. The ``print`` statement displays the value of ``only_vowels`` each
   iteration, and this allows us to see how it changes as the loop repeats.

Reversing a String
------------------

We'll start by initializing two variables: the string we want to reverse, and a variable that will eventually store the reversed value of the given string.

.. sourcecode:: js
   :linenos:

   let str = "accumulator";
   let reversed = "";

Here, ``reversed`` is our accumulator variable. Our approach to reversing the string will be to loop over ``str``, adding each subsequent character to the *beginning* of ``reversed``, so that the first character becomes the last, and the last character becomes the first.

.. admonition:: Example

   .. sourcecode:: js
      :linenos:

      let str = "blue";
      let reversed = "";

      for (let i = 0; i < str.length; i++) {
         reversed = str[i] + reversed;
      }

      console.log(reversed);

   **Console Output**

   ::

      eulb

Notice that we don't use the ``+=`` operator within the loop, since ``reversed += str[i]`` is the same as ``reversed = reversed + str[i]``.

Let's break this down step-by-step. This table shows the values of each of our variables *after* each loop iteration.

.. list-table:: The accumulator pattern, step by step
   :header-rows: 1

   * - Loop iteration
     - ``i``
     - ``str[i]``
     - ``reversed``
   * - (before first iteration)
     - not defined
     - not defined
     - ``""``
   * - 1
     - 0
     - ``"b"``
     - ``"b"``
   * - 2
     - 1
     - ``"l"``
     - ``"lb"``
   * - 3
     - 2
     - ``"u"``
     - ``"ulb"``
   * - 4
     - 3
     - ``"e"``
     - ``"eulb"``

.. admonition:: Try It!

   What happens if you reverse the order of of the assignment statement within the ``for`` loop, so that ``reversed = reversed + str[i];``?

   `Try it at repl.it. <https://repl.it/@launchcode/Reversing-a-string>`_
