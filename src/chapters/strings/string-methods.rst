String Methods
==============

The ``str`` data type includes a special group of operations, called *methods*,
that we can use to make routine tasks easier. A method performs a specific
action on the data within an object. For strings, the methods usually create a
new string from the characters of the original.

Python provides many useful methods for string objects. 

As we learned, strings are immutable. Therefore, string methods will NOT change
the value of a string itself. Instead, they *return* a new string that is the
result of the operation.

We saw this behavior in the ``.lower()`` example.

.. admonition:: Example

   .. sourcecode:: python
      :linenos:

      nonprofit = "LaunchCode"

      print(nonprofit.lower())
      print(nonprofit)

   **Console Output**

   ::

      launchcode
      LaunchCode

While ``nonprofit.lower()`` evaluated to ``"launchcode"``, the value of
``nonprofit`` stayed the same. This will be case for every string method.

Common String Methods
---------------------

.. index::
   single: string; methods

Here we present the most commonly-used string methods. Clicking on the name of
any method leads to examples and a more detailed description.

.. list-table:: Common String Methods
   :header-rows: 1

   * - Method
     - Syntax
     - Description
   * - :ref:`count <string-count-examples>`
     - ``string_name.count(search_string)``
     - Returns the number of times ``search_string`` occurs in ``string_name``.
   * - :ref:`find <string-find-examples>`
     - ``string_name.find(a_string)``
     - Returns the index of the first occurrence of ``a_string`` in
       ``string_name``. The method returns -1 if ``a_string`` is not found.
   * - :ref:`index <string-find-examples>`
     - ``string_name.index(a_string)``
     - Returns the index of the first occurrence of ``a_string`` in
       ``string_name``. If ``a_string`` is not found, the method throws an
       error.
   * - :ref:`lower <string-lower-examples>`
     - ``string_name.lower()``
     - Returns a copy of the given string, with all uppercase letters converted
       to lowercase.
   * - :ref:`replace <string-replace-examples>`
     - ``string_name.replace(original, replacement)``
     - Returns a copy of ``string_name`` with every occurrence of the
       ``original`` string replaced by the ``replacement`` string.
   * - :ref:`split and list <string-split-examples>`
     - ``string_name.split(character)``
     - Splits the string at each occurrence of ``character``, and returns a
       list of smaller strings.
   * - :ref:`strip <string-strip-examples>`
     - ``string_name.strip(character)``
     - Returns a copy of the given string with leading and trailing
       ``character`` strings removed. By default, ``character`` is a space.
   * - :ref:`upper <string-upper-examples>`
     - ``string_name.upper()``
     - Returns a copy of the given string, with all lowercase letters converted
       to uppercase.

You can find complete lists of the Python string methods at:

- `W3Schools <https://www.w3schools.com/python/python_ref_string.asp>`__
- `docs.python.org <https://docs.python.org/3/library/stdtypes.html?highlight=lower#string-methods>`__

.. admonition:: Tip

   String methods can be combined in a process called **method chaining**.
   Given ``word = 'Python'``:
   
   #. ``word.upper()`` returns ``PYTHON``.
   #. ``word.replace('n', 'n!!!')`` returns ``Python!!!``
   
   Chaining the methods together as ``word.replace('n', 'n!!!').upper()``
   returns ``PYTHON!!!``.
   
   What would ``word.lower().strip('p').find('t')`` return?

Check Your Understanding
------------------------

Follow the links in the table above for the ``replace``  and ``strip`` methods.
Review the content and then answer the following questions.

.. admonition:: Question

   What is printed by the following code?

   .. sourcecode:: python
      :linenos:

      text = "Python rocks!"
      text.replace('o', 'q')
      text.strip('!P')
      print(text)

   #. ``Pythqn rocks``
   #. ``Python rqcks``
   #. ``ythqn rqcks!``
   #. ``ythqn rqcks``

.. Answer: d

.. admonition:: Question

   Given ``language = 'Python``, what does ``language[1,4]`` return?

   #. ``"Pyth"``
   #. ``"Pyt"``
   #. ``"yth"``
   #. ``"ytho"``

.. Answer: d

.. admonition:: Question

   What is the value of the string printed by the following program?

   .. sourcecode:: python
      :linenos:

      org = "  The LaunchCode Foundation "
      trimmed = org.strip()

      print(trimmed)

   #. ``"  The LaunchCode Foundation "``
   #. ``"The LaunchCode Foundation"``
   #. ``"TheLaunchCodeFoundation"``
   #. ``" The LaunchCode Foundation"``

.. Answer: b

.. admonition:: Question

   Given ``word = "Rutabaga"`` is the value returned by
   ``word.lower().strip('r').find('t')``?

   #. ``'utabaga'``
   #. ``2``
   #. ``1``
   #. ``'t'``

.. Answer: c
   