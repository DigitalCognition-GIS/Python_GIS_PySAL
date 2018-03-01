# Python_GIS_PySAL
Python_GIS_PySAL

## Initial Hiccups with installations 

---------------------------------------------------------------------------
ImportError                               Traceback (most recent call last)
<ipython-input-1-78e95335453d> in <module>()
----> 1 import pysal
      2 import geopandas
      3 import fiona

ImportError: No module named pysal

[I 23:40:59.723 NotebookApp] Kernel shutdown: 4d8095a8-9aac-4587-9de3-7bbc7339f589
(gisenv) dhankar@dhankar-VPCEB44EN:~/Desktop/Geo_1$ 
(gisenv) dhankar@dhankar-VPCEB44EN:~/Desktop/Geo_1$ python
Python 3.4.5 |Continuum Analytics, Inc.| (default, Jul  2 2016, 17:47:47) 
[GCC 4.4.7 20120313 (Red Hat 4.4.7-1)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
>>> import pysal
>>> 
>>> import geopandas
Traceback (most recent call last):
  File "/home/dhankar/anaconda2/envs/gisenv/lib/python3.4/site-packages/pandas/__init__.py", line 26, in <module>
    from pandas._libs import (hashtable as _hashtable,
  File "/home/dhankar/anaconda2/envs/gisenv/lib/python3.4/site-packages/pandas/_libs/__init__.py", line 4, in <module>
    from .tslib import iNaT, NaT, Timestamp, Timedelta, OutOfBoundsDatetime
ImportError: No module named 'pandas._libs.tslib'

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/home/dhankar/anaconda2/envs/gisenv/lib/python3.4/site-packages/geopandas/__init__.py", line 1, in <module>
    from geopandas.geoseries import GeoSeries
  File "/home/dhankar/anaconda2/envs/gisenv/lib/python3.4/site-packages/geopandas/geoseries.py", line 5, in <module>
    from pandas import Series
  File "/home/dhankar/anaconda2/envs/gisenv/lib/python3.4/site-packages/pandas/__init__.py", line 35, in <module>
    "the C extensions first.".format(module))
ImportError: C extension: No module named 'pandas._libs.tslib' not built. If you want to import pandas from the source directory, you may need to run 'python setup.py build_ext --inplace --force' to build the C extensions first.
>>> 
>>> 

