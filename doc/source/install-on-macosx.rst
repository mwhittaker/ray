Installation on Mac OS X
========================

Ray should work with Python 2 and Python 3. We have tested Ray on OS X 10.11 and
10.12.

Dependencies
------------

To install Ray, first install the following dependencies. We recommend using
`Anaconda`_.

.. _`Anaconda`: https://www.continuum.io/downloads

.. code-block:: bash

  brew update
  brew install cmake automake autoconf libtool boost wget

  pip install numpy cloudpickle funcsigs colorama psutil redis flatbuffers --ignore-installed six

If you are using Anaconda, you may also need to run the following.

.. code-block:: bash

  conda install libgcc


Install Ray
-----------

Ray can be built from the repository as follows.

.. code-block:: bash

  git clone https://github.com/ray-project/ray.git
  cd ray/python
  python setup.py install --user


Test if the installation succeeded
----------------------------------

To test if the installation was successful, try running some tests. This assumes
that you've cloned the git repository.

.. code-block:: bash

  python test/runtest.py
