``split`` and ``join``
======================

Two of the most useful methods involving lists and strings are the methods
``split`` and ``join``. The ``split`` method applies to strings, and it breaks
a string into a list of words. By default, any number of whitespace characters
is considered a word boundary.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      text = "Do what you can, with what you have, where you are."
      words = text.split()
      print(words)
      print(len(words))

   **Console Output**

   ::

      ['Do', 'what', 'you', 'can,', 'with', 'what', 'you', 'have,', 'where', 'you', 'are.']
      11

.. index:: delimiter

We can place an optional argument, called a *delimiter*, inside the ``()``. The
delimiter sets the characters to use as word boundaries. The following example
uses the string ``se`` as the delimiter:

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      text = "Be yourself. Everyone else is already taken."
      words = text.split('se')
      print(words)

   **Console Output**

   ::

      ['Be your', 'lf. Everyone el', ' is already taken.']
      3

Notice that the delimiter does NOT appear in the result.

The opposite of the ``split`` method is ``join``, which is used on a list. The
method takes all of the elements from the list, combines them, and returns a
new string value. To use ``join``, we must give Python a *connector* string to
place between the list elements.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      words = ['Hello', 'how', 'are', 'you?']
      connector = '-'
      new_string = connector.join(words)
      print(words)

      print('***'.join(words))
      print(''.join(words))

   **Console Output**

   ::

      Hello-how-are-you?
      ['Hello', 'how', 'are', 'you?']
      Hello***how***are***you?
      Hellohowareyou?

Note that the original list (``words`` in this example) remains unchanged. Also,
we can use the empty string, whitespace characters (like ``' '`` or ``'\n'``)
or multi-character strings as the connector.

Try It!
^^^^^^^

Lorem ipsum... (Retrieve initials from a name, or reverse the characters from
a string).

List Type Conversion
--------------------

Lorem ipsum...
