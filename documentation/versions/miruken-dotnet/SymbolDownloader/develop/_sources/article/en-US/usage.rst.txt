=======
Usage
=======

Once the SymbolDownloader Powershell Module is installed you should be able to use from a command prompt in any directory.

Download a single package
-------------------------

.. code-block:: powershell
	
	get-symbols Miruken 1.4.0.3

You must provide the package name, and the version number.  This can be done from the commandline in any directory.

.. important:: 
	Package names are case sensitive.

Download symbols in a solution
------------------------------

If you are in a directory that contains packages.config files such as a solution or project directory,
SymbolDownloader can read the packages.config files and download the symbols for specific versions of
the packages you specify.  It does a case insensitive contains on the package name.

.. code-block:: powershell

	get-symbols miruken

Will download the symbols and source for miruken, miruken.castle, miruken.mvc, miruken.mediator, etc...

.. code-block:: powershell

	get-symbols miruken.mediator

Will download the symbols for miruken.mediator and miruken.mediator.castle

This is all provided that the packages.config files contain references to these packages.

.. code-block:: powershell

	get-symbols castle

Will download miruken.castle, castle.core, castle.windsor, etc

It is recusive based on the working directory of the console, so you can run it in a project directory and it will 
only download packages referenced in that project, or you can run it in the solution and download
symbols for all projects.
