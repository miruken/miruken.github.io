==========================
Configuring Castle Windsor
==========================

The first thing we need to do when configuring Castle Windsor is add a reference to the Miruken.Castle nuget package::

	Install-Package Miruken.Castle

.. note:: Full documentation covering Miruken.Castle is `here <http://miruken-dotnet-miruken.readthedocs.io/en/develop/article/en-US/configuration/configuringCastleWindsor.html>`_.

Installing Mediator
===================

The MediatorInstaller lives in Miruken.Mediate.Castle so add a reference to its nuget package::

	Install-Package Miruken.Mediate.Castle

In the Container.Install() method, add your feature assemblies, and then pass in an instance of MediatorInstaller. 

.. literalinclude:: ../../examples/configuration/installingMediator.cs
   :emphasize-lines: 19-21

Installing Validation Middleware
================================

The ValidationInstalling lives in the Miruken.Validate.Castle so add a reference to its nuget package::

	Install-Package Miruken.Validate.Castle

In the Container.Install() method, add your feature assemblies, and then pass in an instance of ValidationInstaller. 

.. literalinclude:: ../../examples/configuration/installingValidateMiddleware.cs
   :emphasize-lines: 20-23

