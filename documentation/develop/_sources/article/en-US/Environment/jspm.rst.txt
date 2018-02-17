====
JSPM
====

Developing Locally 
==================

In the local package directory run :code:`jspm link` to make they package available localy to other packages.

.. code-block:: none

    jspm link

In a different package directory, install the package with the :code:`--link` option.

.. code-block:: none

    jspm install --link npm:miruken-core
