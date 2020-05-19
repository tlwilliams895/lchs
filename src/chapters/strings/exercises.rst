Strings: Exercises
==================

Part One: Brackets Notation
---------------------------

#. Identify the result for each of the following statements:

   a. ``'Characters'[8]``
   b. ``"Strings are sequences of characters."[5]``
   c. ``len("Wonderful")``
   d. ``len("Do spaces count?")``

   *There's no code snippet for this one, just try it on your own with
   old-fashioned pencil and paper!*

#. Use bracket notation to:

   a. Print a slice of the first 12 characters from
      ``"Strings_are_sequences_of_characters."``
   b. Print a slice of the last 12 characters from the same string. You should
      NOT have to count the index values yourself!
   c. Print a slice of the middle 12 characters from the same string.

   `Code it at repl.it <https://repl.it/@launchcode/StringExercises02/>`__

Part Two: String Methods
------------------------

#. The ``len()`` function returns the number of characters in a string. However,
   the function will NOT give us the length of a number. If ``num = 1001``,
   ``len(num)`` throws an error instead of returning ``4``.

   a. Use type conversion to print the length (number of digits) of an integer.
   b. Modify your code to print the number of digits in a ``float`` value (e.g.
      ``num = 123.45`` has 5 digits but a length of 6). The digit count should
      NOT include the decimal point.
   c. What if ``num`` could be EITHER an integer or a decimal? Add an ``if/else``
      statement so your code can handle both cases.  (Hint: Consider using the
      ``find()`` method or the ``in`` operator to check if ``num`` contains a
      decimal point).

   `Code it at repl.it <https://repl.it/@launchcode/StringExercises02/>`__

#. Given ``word = 'bag'``:

   a. Set up a loop to iterate through the string of lowercase vowels,
      ``'aeiou'``.
   b. Inside the loop, create a new string from ``word``, but with a different
      vowel. Use the ``replace`` string method.
   c. Print the new string.
   d. Properly done, your output should look something like this:

      ::

         bag
         beg
         big
         bog
         bug
   
   e. Rerun the program, but use ``'petting'`` instead of ``'bag'``.

   `Code it at repl.it <https://repl.it/@launchcode/StringExercises02/>`__

#. Remember, strings are *immutable*. Consider a string that represents a
   strand of DNA: ``dna = " TCG-TAC-gaC-TAC-CGT-CAG-ACT-TAa-CcA-GTC-cAt-AGA-GCT    "``.
   There are some typos in the string that we would like to fix:

   a. Use the ``trim()`` method to remove the leading and trailing whitespace,
      and then print the result.
   b. Change all of the letters in the dna string to UPPERCASE and print the
      result.
   c. Note that if you try ``print(dna)`` after applying the methods, the
      original, flawed string is displayed. To fix this, you need to
      *reassign* the changes back to ``dna``. Apply these fixes to your
      code so that ``print(dna)`` prints the DNA strand in UPPERCASE
      with no whitespace.

   `Code it at repl.it <https://repl.it/@launchcode/StringExercises03/>`__

#. Let's use string methods to do more work on the DNA strand:

   a. Replace the gene ``'GCT'`` with ``'AGG'``, and then print the altered
      strand.
   b. Look for the gene ``'CAT'`` with ``find()``. If found print, ``'CAT gene
      found'``, otherwise print, ``'CAT gene NOT found'``.
   c. Use ``count()`` to find the number of hyphens (``-``) in the string, then
      print the number of *genes* (sets of 3 letters) in the dna strand. Note
      that the number of genes will be 1 more than the number of hyphens. 
   d. Make your output look something like, ``"The DNA string is ___ characters
      long and contains ___ genes."``

   `Code it at repl.it <https://repl.it/@launchcode/DNA-strings/>`__

Part Three: String Formatting
-----------------------------

Lorem ipsum...
