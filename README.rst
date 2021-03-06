Versioner
=========

Versioner is a very basic Python command-line tool and library to keep
track of the version of your project, any kind of project.

Installation
------------

You can install the last stable release of Versioner using pip:

::

    $ pip install versioner

Usage
-----

Its usage is very simple. If you run ``versioner`` without arguments, it will
print the version currently stored in a file named ``VERSION`` in the current
folder. If such file does not exist, ``versioner`` creates it with an initial
version of 0.0.1:

::

    $ versioner
    0.0.1
    $ cat VERSION
    0.0.1

Versioner accepts a series of arguments to increase, decrease and set
the three diferent categories, you can increase the major version number
with:

::

    $ versioner +major
    1.0.1

Or decrease the revision number with:

::

    $ versioner -revision
    1.0.0

Or directly set the value of each component:

::

    $ versioner minor=2 revision=5
    1.2.5

All this operations will update the ``VERSION`` file. As you can see,
Versioner uses a three-digit versioning schema,
``major.minor.revision``, which should fit most needs. At the end of the
day, if you need a different or more robust versioning schema, chances
are you have the knowledge to build a more suitable tool yourself - or
send a patch!
