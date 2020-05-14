Template Literals
=================

Earlier, we used *concatenation* to combine strings and variables together in
order to create a specific output:

.. todo:: Add an internal book link here to the concatenation section!

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      name = Jack
      current_age = 9

      print("Next year, " + name + " will be " + str(current_age + 1) + ".")

   **Console Output**

   ::

      Next year, Jack will be 10.

   Note the following:
   
   #. We must include spaces inside each of the strings to make the output
      look right. Without the spaces, line 4 prints ``Nextyear,Jackwillbe10.``
   #. In order to concatenate, we must convert the ``int`` value from the
      expression ``current_age + 1`` into the ``str`` data type.

While it does work, concatenation quickly gets tedious for any output that
depends on multiple variables. Also, concatenation usually requires several
test runs of the code in order to check for syntax errors and proper spacing.
Fortunately, Python offers us a better way to accomplish the same thing.

.. index:: ! template literal

**Template literals** allow for the automatic insertion of expressions and
variable values into strings.

Within a template literal, type the output you want, but leave *placeholders*
where you want to insert values. Placeholders are identified by using a pair of
curly braces, ``{}``. When the program runs, the placeholders are replaced by
the values we want to include in the string.

Let's compare the string concatenation in the example above to a template
literal:

.. sourcecode:: python

   # Concatenation
   "Next year, " + name + " will be " + str(current_age + 1) + "."

   # Template literal
   "Next year, {} will be {}."

The braces ``{}`` indicate where we want to insert the values for ``name`` and
``current_age + 1``. Note how we only need one pair of quotes, and the spacing
fits naturally with the {}. Python also takes care of any data type
conversions.

The ``format()`` Method
-----------------------

Template literals allow us to insert variables and other expressions directly
into strings. To accomplish this, we need:

#. A string that includes curly braces ``{}``.
#. The ``.format()`` method.
#. A value to insert into each set of braces.

The general syntax is:

.. sourcecode:: python

   string_with_braces.format(value_1, value_2, etc.)

The values inside the () may be actual numbers or strings, but they will most
often be variables or expressions.

.. admonition:: Example

   Compare the difference between printing ``output`` by itself vs. printing
   ``output.format()``.

   .. sourcecode:: python
      :linenos:

      name = "Jack"
      current_age = 9
      output = "Next year, {} will be {}."

      print(output)
      print(output.format(name, current_age + 1))

   **Console Output**

   ::

      Next year, {} will be {}.
      Next year, Jack will be 10.

Python works from left to right through the string, replacing each placeholder
with the next value inside ``format()``.

.. admonition:: Try It!

   .. todo:: Insert interactive .format() repl here!!!

   Experiment with the ``format()`` string method.

   #. Do this...
   #. Do this...
   #. Do this...
   #. Mismatched {} and values.

   .. sourcecode:: python
      :linenos:

      my_string = 'Hello'
      my_number = 3
      my_expression = my_string * my_number
      
      output = '''This is my_string: {}. 
      This is a my_number: {}.
      This is the length of my_string * my_number: {}'''

      print(output.format(my_string, my_number, len(my_expression))

Indexes in ``format()``
^^^^^^^^^^^^^^^^^^^^^^^

Lorem ipsum...

f-Strings
---------

Lorem ipsum...

Zen of Python
-------------

   Beautiful is better than ugly, 
   Simple is better than complex,
   Readability counts.

Check Your Understanding
------------------------

.. admonition:: Question

   Mad Libs are games where one player asks the group to supply random words
   (e.g. "Give me a verb," or, "I need a color"). The words are substituted
   into blanks within a story, which is then read for everyone's amusement. In
   elementary school classrooms, giggles and hilarity often ensue. TRY IT!

   Refactor the following code to replace the awkward string concatenation with template literals. Be sure to add your own choices for the variables.

   .. sourcecode:: python
      :linenos:

      pluralNoun = ''
      name = ''
      verb = ''
      adjective = ''
      color = ''

      print("Python provides a "+ color +" collection of tools — including " + adjective + " syntax and " + pluralNoun + " — that allows "+ name +" to "+ verb +" with strings.")
