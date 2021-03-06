============================
Delft3D Flexible Mesh Python
============================


.. image:: https://img.shields.io/pypi/v/delft3dfmpy.svg
        :target: https://pypi.python.org/pypi/delft3dfmpy

.. image:: https://img.shields.io/travis/grongen/delft3dfmpy.svg
        :target: https://travis-ci.org/grongen/delft3dfmpy

.. image:: https://readthedocs.org/projects/delft3dfmpy/badge/?version=latest
        :target: https://delft3dfmpy.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status




Python package to generate delft3dfm models from standardized data models or other flow models.


* Free software: MIT license
* Documentation: https://dhydamo.readthedocs.io.


Features
--------

* Read Hydamo or shape files to Python data structure
* Build Delft3D RR/FM model from Hydamo or seperately defined elements
* Generate rectangular meshes with refinement
* Create 1D 2D connections
* Genererate an rainfall-runoff model from raster input
* Write to Delft3D FM model, coupled with RR or standalone

Note that the RR-part has been newly developed and it not yet fully tested, especially on larger catchments. It is able to produce a complete, running model for the Moergestelsbroek (see notebooks/), but no larger areas has been modelled yet.

Installation
------------
This module cannot be installed with pip or conda. To use it:

1.  Clone or download the repository;

2.  To import the delft3dfmpy module in your script or notebook, Python needs to find the delft3dfmpy module on one of the following directories:

    * the Python working directory. This can be checked in Python with::

        import os
        print(os.getcwd())

    * the site-packages directory of the Python installation in the correct environment (see below). Using anaconda, this is usually C:/users/[name]/AppData/Local/Continuum/Anaconda3/envs/delft3dfmpy/Lib/site-packages

    * a user defined directory, added within the script with::

        import sys
        sys.path.append('path/to/directory')

    If the downloaded directory is named "delft3dfmpy-master", rename it to "delft3dfmpy"

To get all the required dependencies working, it is advised to:

1.  Install a Anaconda Python distribution: https://www.anaconda.com/distribution/

2.  Create an environment with the required modules, by executing the following commands in an anaconda command prompt::

        conda config --add channels conda-forge
        conda create --name delft3dfmpy numpy scipy matplotlib pandas geopandas gdal=2.4.1 rasterio netcdf4 pillow

3.  Activate the created environment in an anaconda command prompt (activate delft3dfmpy) before running your notebook or script. A jupyter notebook or command prompt for the environment can also be launched from the Anaconda Navigator.

4.  For more information on how to use environments, see: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

Usage
-----
The usage is best described by the example notebook: https://github.com/openearth/delft3dfmpy/blob/master/notebooks/Usage_introduction_coupled_RRFM.ipynb
