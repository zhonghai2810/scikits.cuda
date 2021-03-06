.. -*- rst -*-

Installation
============

Quick Installation
------------------
If you have `pip <http://pypi.python.org/pypi/pip>`_ installed, you should be
able to install the latest stable release of ``scikits.cuda`` by running the
following::

   pip install scikits.cuda

All dependencies should be automatically downloaded and installed if they are
not already on your system.

Obtaining the Latest Software
-----------------------------
The latest stable and development versions of ``scikits.cuda`` can be downloaded 
from `GitHub <https://github.com/lebedov/scikits.cuda>`_

Online documentation for ``scikits.cuda`` is available at 
`<https://scikit-cuda.readthedocs.org>`_

Installation Dependencies
-------------------------
``scikits.cuda`` requires that the following software packages be
installed:

* `Python <http://www.python.org>`_ 2.6 or later (some parts of the package may
  not work with Python 3).
* `setuptools <http://pythonhosted.org/setuptools>`_ 0.6c10 or later.
* `NumPy <http://www.numpy.org>`_ 1.2.0 or later.
* `PyCUDA <http://mathema.tician.de/software/pycuda>`_ 2013.1 or later (some
  parts of ``scikits.cuda`` might not work properly with earlier versions).
* `NIVIDIA CUDA Toolkit <http://www.nvidia.com/object/cuda_home_new.html>`_ 5.0 or later.

To run the unit tests, the following packages are also required:

* `nose <http://code.google.com/p/python-nose/>`_ 0.11 or later.
* `SciPy <http://www.scipy.org>`_ 0.9.0 or later.

Some of the linear algebra functionality relies on the CULA Dense toolkit; the 
single precision release of the toolkit is free of charge, but requires 
registration.  Depending on the version of CULA installed, some functions may 
not be available:

* `CULA <http://www.culatools.com/dense/>`_ R16a or later.

To build the documentation, the following packages are also required:

* `Docutils <http://docutils.sourceforge.net>`_ 0.5 or later.
* `Jinja2 <http://jinja.pocoo.org>`_ 2.2 or later.
* `Pygments <http://pygments.org>`_ 0.8 or later.
* `Sphinx <http://sphinx.pocoo.org>`_ 1.0.1 or later.
* `Sphinx ReadTheDocs Theme
  <https://github.com/snide/sphinx_rtd_theme>`_ 0.1.6 or later.

Platform Support
----------------
The software has been developed and tested on Linux; it should also 
work on other Unix-like platforms supported by the above packages. Parts of the
package may work on Windows as well, but remain untested.

Building and Installation
-------------------------
``scikits.cuda`` searches for CUDA libraries in the system library
search path when imported. You may have to modify this path (e.g., by adding the
path to the CUDA libraries to ``/etc/ld.so.conf`` and running ``ldconfig`` as 
root or to the
``LD_LIBRARY_PATH`` environmental variable on Linux) if the libraries are
not being found.

To build and install the toolbox, download and unpack the source 
release and run::

   python setup.py install

from within the main directory in the release. To rebuild the
documentation, run::

   python setup.py build_docs

Running the Unit Tests
----------------------
To run all of the package unit tests, download and unpack the package source
tarball and run::

   nosetests

from within the main directory in the archive. Tests for individual
modules (found in the ``tests/`` subdirectory) can also be run
directly.

Getting Started
---------------
The functions provided by ``scikits.cuda`` are grouped into several submodules 
in the ``scikits.cuda`` namespace package. The ``skcuda`` namespace package is 
also provided as a shortcut to ``scikits.cuda``. Sample code demonstrating how 
to use different parts of the toolbox is
located in the ``demos/`` subdirectory of the source release. Many of the 
high-level functions also contain doctests that describe their usage.

