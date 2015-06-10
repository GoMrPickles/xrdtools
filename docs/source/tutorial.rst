Quick start tutorial
--------------------

The main functionality of the **xrdtools** package is to read *.xrdml* files. This can be
easily achieved by running the following code, e.g. in a ipython prompt::

    >>> import xrd
    >>> data = xrd.read_xrdml('foo.xrdml')

The data returned from :func:`xrd.read_xrdml` is stored in a :obj:`dict`. In case of a simple line scan
(e.g. *2theta-omega* scan) we can get the *xy* data as simple as::

    >>> x = data['x']
    >>> y = data['y']

And plot it for example with :py:mod:`matplotlib.pyplot`::

    >>> from matplotlib import pyplot as plt
    >>> plt.plot(x, y)
    >>> plt.show()