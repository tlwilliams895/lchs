``for`` Syntax
==============

Flow of Execution of the ``for`` Loop
-------------------------------------

In just a few lines of code, a ``for`` loop contains a lot of detailed logic,
so let's spend some time breaking down the flow of execution for the particular
loop that we've been looking at.

.. sourcecode:: python
   :linenos:

   for (let i = 0; i < 51; i++) {
      console.log(i)
   }

Here is a step-by-step description of how this loop executes:

#. When the program reaches the ``for`` loop, the initial expression ``let i = 0`` is executed, declaring the variable ``i`` and initializing it to the value ``0``.
#. The loop condition ``i < 51`` is evaluated, returning ``true`` because 0 is
   less than 51.
#. Since the condition is ``true``, the loop body executes, printing 0.
#. After the execution of the loop body, the update expression ``i++`` is executed, setting ``i`` to 1. This completes the first iteration of the loop.
#. Steps 2 through 4 are repeated, using the new value of ``i``. This continues until the loop condition evaluates to ``false`` in step 2, ending the loop. In this example, this occurs when ``i < 51`` is ``false`` for the first time. Since our update expression adds 1 after each iteration, this occurs when ``i`` is 51 (so ``51 < 51`` is ``false``). At that point, the loop body will have executed exactly 51 times, with ``i`` having the values 0...50.

In general, we can visualize the flow of execution of a ``for`` loop as a flowchart.

   FIGURE HERE!!!!
