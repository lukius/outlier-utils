=============
outlier-utils
=============

.. image:: https://travis-ci.org/c-bata/outlier-utils.svg
    :target: https://travis-ci.org/c-bata/outlier-utils


.. image:: https://coveralls.io/repos/c-bata/outlier-utils/badge.svg?branch=master&service=github
  :target: https://coveralls.io/github/c-bata/outlier-utils?branch=master

This is the library for removing outliers.

- Smirnov Grubbs Tests

::

   >>> from outliers import smirnov_grubbs as grubbs
   
   >>> import pandas as pd
   >>> data = pd.Series([1, 8, 9, 10, 9])
   >>> grubbs.test(data, 0.05)
   1     8
   2     9
   3    10
   4     9
   dtype: int64
   
   >>> import numpy as np
   >>> data = np.array([1, 8, 9, 10, 9])
   >>> grubbs.test(data, 0.05)
   [ 8  9 10  9]


Requirements
============

* Traget Python version is 2.7, 3.4
* numpy / scipy / pandas


License
=======

This software is licensed under the MIT License.