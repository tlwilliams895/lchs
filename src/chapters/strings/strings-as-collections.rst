Strings as Collections
======================

Throughout the first chapters of this book we used strings to represent words,
phrases, or characters we wanted to print out. Our definition of a string was
simple: *a string is a sequence of characters inside quotes*.

In this chapter we explore strings in much more detail.

Collection Data Types
---------------------

.. index:: ! collection

.. index::
   single: data type; collection

Strings are an example of a **collection data type**. *Collections* are built
from smaller, individual pieces. Other data types like ``int``, ``float``, and
``bool`` do NOT contain any smaller parts.

Depending on what we are doing, we can treat a collection data type as a single
object, like a cardboard box, or we can dig into the collection and access its
smaller parts (searching through the box).

.. index:: ! character

A **character** is a string that contains exactly one element, such as ``'a'``,
``"?"``, or even ``" "`` (a single space character).

Strings are built out of these single characters. In this way, strings can be
broken down into smaller pieces.

   [INSERT PYTHON CHARACTER DIAGRAM HERE!!!!]

.. todo:: Add the Python character figure here.

   A string is made up of characters, which are strings of length 1.

Ordered Collections
-------------------

.. index::
   single: collection; ordered

We also call strings **ordered collections** of characters. This means that the
individual characters in the string follow a particular order from left to
right. The string ``"LaunchCode"`` is different from the string
``"CodeLaunch"``, even though they contain the exact same characters.

Quote Reminder
--------------

Recall from the Data and Variables chapter that we can use single quotes around
a string (``'hello'``), double quotes (``"hello"``), or triple quotes
(``'''hello'''`` and ``"""hello"""``), as long as we start and end with the
same type.

.. todo::

   Add an internal book link here to the relevant section of the Data and
   Variables chapter.

Why have three options?

#. We can include quote characters inside a string, as long as we use a
   different type around the entire collection. For example, ``"The teacher's
   classroom."`` or ``'''"Quote from a book, with the author's name."'''``).
#. Triple quotes allow us to create strings that cover multiple lines.

   .. sourcecode:: Python
      :linenos:

      sentence = '''This string covers
      multiple lines.
      Cool!'''

      print(sentence)

   **Console Output**

   ::

      This string covers
      multiple lines.
      Cool!
