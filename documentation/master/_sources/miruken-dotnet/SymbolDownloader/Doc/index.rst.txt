=================
Symbol Downloader
=================

.. image:: img/miruken_circle_net.png

Visual Studio (VS) supports debugging with symbol files out of the box.  Resharper also supports debuging with symbol files.  However, the process of downloading the files has proven to be frustrating and unreliable.  There are at least 3 major issues we've identified when trying to download symbols and source files with Visual Studio and they all require restarting Visual Studio.

1. VS will stop trying to download symbols if it has already tried once and failed.

2. VS will hange trying to download the .pdb file and never ask for the .pd_ file which is what https://nuget.smbsrc.net actually serves. 

3. VS will not try to load symbols immediately after a new package is added.

To solve these problem, SymbolDownloader downloads .pdb, .pd_ files,  and all associated source files for a nuget package independently of Visual Studio.

.. toctree::
   :maxdepth: 2
   :caption: Table of Contents

   article/en-US/install.rst
   article/en-US/usage.rst
   article/en-US/configuration.rst
   article/en-US/teamCity.rst
