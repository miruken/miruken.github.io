=============
Configuration
=============

You can configure SymbolDownloader to look for symbols on specific servers 
by changing :code:`Source/config.json`.  Here we are looking on the public
nuget servers and mirukens own nuget server.  You can add your own servers
to the list.

.. code-block:: console

	{
		symbolFolder: "c:/temp/symbols",
		nugetServers: [
			"https://www.nuget.org/api/v2/",
	        "http://build.miruken.com/guestAuth/app/nuget/v1/FeedService.svc/",
		],
		symbolServers: [
			"https://nuget.smbsrc.net",
	        "http://build.miruken.com/app/symbols",
		]
	}
