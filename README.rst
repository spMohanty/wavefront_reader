===============================
wavefront_reader
===============================


.. image:: https://img.shields.io/pypi/v/wavefront_reader.svg
        :target: https://pypi.python.org/pypi/wavefront_reader

.. image:: https://travis-ci.org/neuroneuro15/wavefront_reader.svg?branch=master
        :target: https://travis-ci.org/neuroneuro15/wavefront_reader

.. image:: https://readthedocs.org/projects/wavefront-reader/badge/?version=latest
        :target: https://wavefront-reader.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://pyup.io/repos/github/neuroneuro15/wavefront_reader/shield.svg
     :target: https://pyup.io/repos/github/neuroneuro15/wavefront_reader/
     :alt: Updates

A parser for wavefront .obj and .mtl files


* Free software: MIT license
* Documentation: https://wavefront-reader.readthedocs.io.


Features
--------

Reads out wavefront objects to dictionaries with their attributes, including their materials::

    from wavefront_reader import read_wavefront, read_objfile, read_mtlfile
    geoms = read_wavefront('myObjects.obj')
    cube = geoms['Cube']
    cube_vertices = cube['v']
    cube_diffuse_material = cube['material']['Kd']

The module has a lot of tests, and handles face indexing by re-indexing the vertex, normal, and texcoord arrays
simply by reindexing them into same-length, sequential arrays.  While this reduces the memory benefits of the .obj
format, it makes it much easier to load the data into OpenGL or reindex the data yourself.

Credits
---------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage

