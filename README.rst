#####################################
cpplint - static code checker for C++
#####################################

.. image:: https://img.shields.io/pypi/v/cpplint.svg
    :target: https://pypi.python.org/pypi/cpplint

.. image:: https://img.shields.io/pypi/pyversions/cpplint.svg
    :target: https://pypi.python.org/pypi/cpplint

.. image:: https://img.shields.io/pypi/status/cpplint.svg
    :target: https://pypi.python.org/pypi/cpplint

.. image:: https://img.shields.io/pypi/l/cpplint.svg
    :target: https://pypi.python.org/pypi/cpplint

.. image:: https://img.shields.io/pypi/dd/cpplint.svg
    :target: https://pypi.python.org/pypi/cpplint

.. image:: https://img.shields.io/pypi/dw/cpplint.svg
    :target: https://pypi.python.org/pypi/cpplint

.. image:: https://img.shields.io/pypi/dm/cpplint.svg
    :target: https://pypi.python.org/pypi/cpplint

Cpplint is a command-line tool to check C/C++ files for style issues according to `Google's C++ style guide <http://google.github.io/styleguide/cppguide.html>`_.

Cpplint is a friendly fork of Google's original tool at `google/styleguide <https://github.com/google/styleguide>`_. Nowadays, `Google no longer maintains a public version of cpplint <https://github.com/google/styleguide/pull/528#issuecomment-592315430>`_, and many issues and pull requests remain unimplemented.

This fork aims to update cpplint to modern specifications, and be (somewhat) more open to adding fixes and features to make cpplint usable in wider contexts.


Installation
============

Use `pipx <https://pipx.pypa.io>`_ to install cpplint from PyPI, run:

.. code-block:: bash

    $ pipx install cpplint

Or use `uv <https://docs.astral.sh/uv>`_ to install cpplint from PyPI, run:

.. code-block:: bash

    $ uv tool install cpplint

Usage
-----
.. code-block:: bash

    $ cpplint [OPTIONS] files

For full usage instructions, run:

.. code-block:: bash

    $ cpplint --help

cpplint can also be run as a pre-commit hook by adding to `.pre-commit-config.yaml`:

.. code-block:: yaml

  - repo: https://github.com/cpplint/cpplint
    rev: 2.0.2
    hooks:
      - id: cpplint
        args:
          - --filter=-whitespace/line_length,-whitespace/parens

Changes
=======

* Python 3 compatibility
* JUnit XML output format
* More default file extensions
* Continuous integration on GitHub
* Support for excluding files via ``--exclude``
* Customizable file extensions with the ``--extensions`` argument
* Support for recursive file discovery via the ``--recursive`` argument
* Overriding repository root auto-detection via ``--repository``
* Support ``#pragma once`` as an alternative to header include guards
* ... and `quite a bit <https://github.com/cpplint/cpplint/blob/develop/CHANGELOG.rst>`_ more

Acknowledgements
================

Thanks to Google Inc. for open-sourcing their in-house tool.

Thanks to `our contributors <https://github.com/cpplint/cpplint/graphs/contributors>`_.

Maintainers
-----------

* `@aaronliu0130 <https://github.com/aaronliu0130>`_
* `@cclauss <https://github.com/cclauss>`_
* `@jayvdb <https://github.com/jayvdb>`_

Former
^^^^^^

* `@tkruse <https://github.com/tkruse>`_
* `@mattyclarkson <https://github.com/mattyclarkson>`_
* `@theandrewdavis <https://github.com/theandrewdavis>`_
