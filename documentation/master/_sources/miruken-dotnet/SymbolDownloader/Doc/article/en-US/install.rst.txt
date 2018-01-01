=======
Install
=======

Powershell modules are installed by copying the powershell files into a known directory that is on the PSModulePath environment variable.  I like to use:

.. code-block:: console

	C:\Users\<USER_NAME>\Documents\WindowsPowerShell\Modules

Make sure the above directory is in the PSModulePath environment variable. You can read that variable using powershell:

.. code-block:: console

	Get-ChildItem Env:\PSModulePath

Install the module straight from git by:

.. code-block:: console

	cd C:\Users\<USER_NAME>\Documents\WindowsPowerShell\Modules
	git clone https://github.com/Miruken-DotNet/SymbolDownloader.git	

Now open a powershell window in a solution or project directory. 
You should be able to just use the module since it is in a known module folder.
Older versions of powershell would force you to import the module explicitly:

.. code-block:: powershell

	Import-Module SymbolDownloader
	
SymbolDownloader is now ready to use.	
