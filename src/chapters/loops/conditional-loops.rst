Loops With Conditions
=====================

.. TODO: Insert internal link to conditionals chapter here.

In the last chapter, we learned how to use conditionals to decide which block
of code to run. In this chapter, we use loops to repeat a set of statements
multiple times.

You might wonder, *Can I put a loop inside an ``if`` statement*, or *Can I put
a conditional inside a loop?*

The answer to both of these questions is a definite, *YES!*

Repeating a Check
-----------------

Run the following code samples to see how each one behaves.

.. admonition:: Examples

   INSERT 2 REPLS HERE!!!!!

   .. sourcecode:: python
      :linenos:

      num = 20
      word = 'Coding ROCKS!'
      num_vowels = 0

      for number in range(num):
         if number%3 == 0:
            print(number, "is divisible by 3.")
         else:
            print(number, "is NOT divisible by 3.")

      for char in word:
         if char in 'aeiou':
            num_vowels += 1
      
      print(word, "contains", num_vowels, "lowercase vowels.")

In the first loop, the text displayed in the console depends on whether the
condition ``number%3 == 0`` returns ``True``. If ``number`` is evenly divisible
by 3, then line X runs. Otherwise, line X+2 runs.

In the second loop, the condition ``char in 'aeiou'`` returns ``True`` if
the value of ``char`` matches any part of the string. When this happens,
``num_vowels`` gets increased by 1 (line Y). ``Coding ROCKS!`` contains 2
lowercase vowels, so line Y only runs 2 times. For every other character in the
string, the line gets skipped.

.. admonition:: Try It!

   How could you make the second program count both lowercase and uppercase
   vowels?

Looping ``if``
--------------

We can also place a loop inside any of the code blocks of an ``if/elif/else``
statement.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      if condition:
         for var_name in range(value):
            # Loop body
      elif other_condition:
         for char in string:
            # Loop body
      else:
         for step in range(20):
            print("Python ROCKS!")

#. IF ``condition`` is ``True``, the ``for`` loop starting on line 2 runs.
#. IF ``other_condition`` is ``True``, then the loop starting on line 5 runs.
#. IF ``condition`` and ``other_condition`` are both return ``False``, then
   ``Python ROCKS!`` gets printed 20 times by the last loop.

Placing a loop inside a conditional allows us to choose when the loop body
should run.
