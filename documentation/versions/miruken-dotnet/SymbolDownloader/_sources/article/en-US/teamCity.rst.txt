=========
Team City
=========

We use Team City's built in nuget server and symbol server to host prerelease nugets.

Debug and Release Build Configuration
=====================================

We build prerelease nugets with the **Debug** configuration for maximum information while developing.
Release builds are build with the **Release** configuration.  
There seems to be less information available to Release builds when debuging because it get optimized away.

Build Output
============
To make Debug and Release builds work we require that build output be localed in the **bin** folder
not the default **bin/debug** and **bin/release**

Symbol Indexer
==============
Prerelease builds need the **Symbol Indexer** build feature turned on.  It is what adds symbol information
to the pdb file.  If this is not run successfully symbols will not be downloadable.
You know it runs when you see something similar to the following in the build output.

.. code-block:: console
	Indexing sources appeared in file C:\TeamCity\BuildAgents\BuildAgent03\work\ebeb9ff100c9190e\Source\Improving.DbUp\bin\Improving.DbUp.pdb
	[15:52:06]Information about 6 source files was updated

..important::
	Do not add the **Symbol Indexer** to release builds that are being pushed to nuget and SymbolSource.org.
	Dll's have 2 fields that uniquely itentify them.  The **signature** and the **age**.  Running the Symbol Indexer
	will increment the age in the dll and then :code:`nuget.exe` with increment the age again.  The dll age will no longer 
	match and you will not be able to download symbols.


