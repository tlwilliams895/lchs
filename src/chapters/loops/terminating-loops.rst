Ending a Loop With ``break``
============================

.. index:: ! break

Python, like most programming languages, provides a way to stop a loop before it
would normally finish. The ``break`` keyword, when placed within a loop,
immediately stops the execution of the loop. Program flow then continues with
the next line of code below the loop.

.. admonition:: Example

   Line 3 repeats 12 times with values of ``iteration`` from 0 to 11. During the
   twelfth iteration, ``iteration`` is 11 and the condition ``num > 10``
   evaluates to ``True`` for the first time. As a result, the program flow
   reaches the ``break`` statement. The loop immediately stops, even though
   ``range(42)`` would normally keep the loop going.

   .. sourcecode:: python
      :linenos:

      for iteration in range(42):
         
         print('This is iteration number:', iteration+1).

         if iteration > 10:
            break

Why would we need to use ``break``? After all, we tell Python how many times
the loop should repeat in the ``for`` statement?

Consider a
situation where we are searching for a particular word in the dictionary.

The ``break`` statement can also be used within a ``while`` loop. 

We can use a ``while`` loop to say, *while we have not reached the end of the array, continue iterating*. We can then include a ``break`` within a conditional check to say, *when we have found the element we are searching for, exit the loop*.

.. admonition:: Example

   A ``while`` loop can be used with ``break`` to search for an element in an array. 

   .. sourcecode:: js
      :linenos:

      let numbers = [ /* some numbers */ ];
      let searchVal = 42;
      let i = 0;

      while (i < numbers.length) {
         if (numbers[i] === searchVal) {
            break;
         }
         i++;
      }

      if (i < numbers.length) {
         console.log("The value", searchVal, "was located at index", i);
      } else {
         console.log("The value", searchVal, "is not in the array.");
      }

Notice that we use a ``while`` loop in this example, rather than a ``for`` loop. This is because our loop variable, ``i``, is used outside the loop. When we use a ``for`` loop in the way we have been, the loop variable exists only within the loop.
