Coding Style
============

Indentation and Line Endings
++++++++++++++++++++++++++++

This rule applies to all languages and projects.
Always develop with the `Editor Config <http://editorconfig.org/>`_ plugin enabled for your editor.
Refer to the Little Weaver
`.editorconfig <https://github.com/littleweaver/littleweaver/blob/master/Style/.editorconfig>`_
configuration for rules related to indentation and line endings per language.

Python
++++++

We conform to `Django's style guide <https://docs.djangoproject.com/en/dev/internals/contributing/writing-code/coding-style/>`_,
with the following exceptions:

* Projects which do not support Python 2 and Python 3 don't need
  to use compatibility shims.

ES6 / React
+++++++++++

Except as noted below, we conform to the following Airbnb style
guides:

* `Airbnb JavaScript Style Guide <https://github.com/airbnb/javascript>`_
* `Airbnb React/JSX Style Guide <https://github.com/airbnb/javascript/tree/master/react>`_

Semicolons
----------

Never use semicolons unless actually required (though if that
happens reevaluate the choices that have led you to that
point.)

Spacing
-------

Similar to python, module-level objects should be separated by
two blank lines, and class-level objects (like methods) should be
separated by a single blank line. Single blank lines can also be
used to group logically-related items within a function or
otherwise make the code more legible.

Within a set of JSX elements, high-level organizational siblings
should be separated by a blank line.

Imports
-------

Imports should be grouped in four overall sections:

1. System. This will probably not happen in the react app, but
   would include things like babel-polyfill and node imports.
2. Core Libraries. Things our application is really
   foundationally built on, in particular: ``react``, ``react-redux``,
   ``redux``, ``react-router``.
3. Libraries. Any other libraries.
4. Local. Any code from our application.

The four groups should be separated by a single blank line each.
Within each group, imports should be sorted alphabetically by
filename. Imports which destructure more than one item should
always be split onto multiple lines. Destructured items should
be alphabetically ordered. ``import *`` should be avoided as it
makes checks of available variables more difficult and delays
import errors until runtime.

Import paths for local code should always be relative to ``~``
rather than using ``.`` or ``..``.
