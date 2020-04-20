Exercises: Loops
================

.. pull-quote::

   Practice makes better. Repetition is a good thing.

   Repetition is a good thing.

   Repetition is a good thing.

   Repetition is a good thing.

WAIT!!!  Why type "Repetition is a good thing" four times when we can code a
better result?  How about printing the phrase 100 times instead?

.. sourcecode:: python
   :linenos:

   for line in range(100):
      print("Repetition is a good thing.")

Loops simplify repetitive tasks!

``for`` Practice
-----------------

   INSERT REPL.IT LINK HERE!!!

#. Construct ``for`` loops that accomplish the following tasks:

   a. Print the numbers 0 - 20, one number per line.
   b. Print only the ODD values from 3 - 29, one number per line.
   c. Print the EVEN numbers 12 down to -14 in descending order, one number
      per line.
   d. Print the numbers 50 down to 20 in descending order, but only
      if the numbers are multiples of 3.

#. Given the string ``'LaunchCode'``, code two ``for`` loops to do the
   following:

   a. Print each character of the string, one letter per line.
   b. Using ``index`` values, print each character of the string---in reverse
      order---to a new line.

#. Given the string ``gibberish =
   'Vna#hewzB*rQhT%yq^lv %iPwgOexWo &C^oUoGSdtJLj'``, print the first character
   and every 5th character after that. Use index values and
   ``range(start, stop, step)``.

   *Hint*: How can you make Python figure out the ``stop`` value so you won't
   have to count the characters in ``gibberish`` yourself?

#. **Bonus:** Repeat the previous problem, but:

   a. Replace ``range(start, stop, step)`` with ``range(len(gibberish))``.
   b. Use an ``if`` statement and the modulus (``%``) operator to check if the
      index is divisible by 5. If ``True``, print the character. If ``False``,
      do not print the character.

``while`` Practice
-------------------

   INSERT REPL.IT LINK HERE!!!

Define three variables for a spacecraft---one for the starting fuel level,
another for the number of astronauts aboard, and the third for the altitude the
spacecraft reaches.

4. Construct ``while`` loops to do the following:

   #. Prompt the user to enter the starting fuel level. The loop should continue until
      the user enters a positive value greater than 5000 but less than 30000.
   #. Use a second loop to query the user for the number of astronauts
      (up to a maximum of 7). Validate the entry by having the loop continue
      until the user enters an integer from 1 - 7.

#. Use a third ``while`` loop to update the fuel status and the altitude of the
   spacecraft. Each iteration, decrease the fuel level by 100 units for each
   astronaut aboard. Also, increase the altitude by 50 kilometers.
   
   *Hint*: The loop should end when there is not enough fuel to boost the crew
   another 50 km, so the fuel level might not reach 0.

#. After the loops complete, print the result with the phrase, ``The spacecraft
   gained an altitude of ___ km and has ___ kg of fuel left.``

#. **Bonus:** If the altitude is 2000 km or higher, add "Orbit achieved!" to
   the output. Otherwise add, "Failed to reach orbit."

The Accumulator Pattern
-----------------------

Lorem ipsum...
