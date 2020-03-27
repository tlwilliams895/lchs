Variables
=========

.. index:: ! variable

One of the most powerful features of a programming language is the ability to
use variables. A **variable** is a name that refers to a value. Recall that a
value is a single, specific piece of data, such as a specific number or string. Variables allow us to store values for later use.

You can think of a variable as a label that *points to* a piece of data.

   INSERT FIGURE HERE

Caption: The label my_word points to a the string value "Python"

   The variable my_word points to the value "Python".

With this picture in mind, let's learn how to create and use variables in
Python.

Assigning Values
----------------

.. index:: ! assignment statement

**Assignment statements** create new variables and also give them values to
refer to. The syntax for an assignment statement is:

.. sourcecode:: Python

   variable_name = value

The assignment statement links a name, on the left hand side of the ``=``, with
the value on the right hand side. The *value* refers to any type of data.

.. admonition:: Example

   .. sourcecode:: Python

      message = "Python ROCKS!"
      num = 17
      pi = 3.14159

This example makes three assignments. The first assigns the string value
``"Python ROCKS!"`` to a new variable named ``message``. The second gives the
integer ``17`` to ``num``, and the third assigns the float ``3.14159`` to a
variable called ``pi``.

.. admonition:: Warning

   The ``=`` sign does NOT work both ways. ``17 = num`` causes an error. The
   variable name MUST be on the left, and the value MUST be on the right.

One common mistake is to confuse the assignment operator ``=`` with the idea of
equality (things being the same). *Equality* compares two values, like ``5``
vs. ``4`` or ``'dog'`` vs. ``'dog'``. *Assignment* gives a value to a variable.

We will explore *equality* later and see that it uses the ``==`` operator
instead of ``=``.

Evaluating Variables
--------------------

.. index:: variable, evaluation

After we create a variable and assign it a value, we can use the variable later
in place of that value.

.. admonition:: Example

   These two examples give the exact same output.

   .. sourcecode:: python

      print("Hello, World!")

   .. sourcecode:: python
      :linenos:

      message = "Hello, World!"
      print(message)

When we use a variable name like this, we **evaluate** the variable. When
Python sees ``print(message)``, it replaces``message`` with its value.
``print(message)`` means the same thing as ``print("Hello, World!")``, so we
say that ``message`` *evaluates to* ``"Hello, World!"``

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      message = "Python ROCKS!"
      num = 17
      pi = 3.14159

      print(message)
      print(num)
      print(pi)

   **Console Output**

   ::

      Python ROCKS!
      17
      3.14159

In each case, the printed result is the value of the variable. 

Try This
^^^^^^^^

Do variables have data types? Run the following code to find out.

   INSERT REPL BOX HERE

The type of a variable is same as the data type of its current value.

Reassigning Variables
---------------------

We use variables in a program to "remember" things, like the current score at the football game. As their name implies, variables can change over time, just like the scoreboard at a football game. You can assign a value to a variable, and later assign it a different value.

To see this, read and then run the following program in a code editor. You'll notice that we change the value of ``day`` three times, and on the third assignment we even give it a value that is of a different data type.

.. sourcecode:: js
   :linenos:

    let day = "Thursday";
    console.log(day);

    day = "Friday";
    console.log(day);

    day = 21;
    console.log(day);

A great deal of programming involves asking the computer to remember things. For example, we might want to keep track of the number of missed calls on your phone. Each time another call is missed, we can arrange to update a variable so that it will always reflect the correct total of missed calls.

.. note:: We only use ``let`` when *declaring* a variable, that is, when we create it. We do NOT use ``let`` when reassigning the variable to a different value. In fact, doing so will result in an error.

Check Your Understanding
------------------------

.. admonition:: Question

   What is printed when the following code executes?

   .. sourcecode:: js
      :linenos:

       let day = "Thursday";
       day = 32.5;
       day = 19;
       console.log(day);

   1. Nothing is printed. A runtime error occurs.
   2. ``Thursday``
   3. ``32.5``
   4. ``19``

    
.. admonition:: Question

   How can you determine the type of a variable?

   1. Print out the value and determine the data type based on the value printed.
   2. Use ``typeof``.
   3. Use it in a known equation and print the result.
   4. Look at the declaration of the variable. 

.. admonition:: Question

   Which line is an example of variable initialization? (*Note: only one line is such an example.*)

   .. sourcecode:: js
      :linenos:
      
      let a;
      a = 42;
      a = a + 3;

