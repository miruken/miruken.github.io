========
Overview
========

Source Code
===========

`github.com/miruken-dotnet/Miruken.Mediate <https://www.github.com/miruken-dotnet/Miruken.Mediate>`_

Installation
============

Install into your project using Nuget::

	Install-Package Miruken.Mediate

Mediator Pattern
================

The mediator pattern allows us to implement cross cutting concerns like error handling, logging, validation, and caching in a pipline that is portable between applications.  Asp.net has a pipeline, but it is tied to the web.  NServiceBus gives us a message handling pipeline, but that is tied specifically to NserviceBus. WCF also has a pipeline you can use, but it is only in WCF.  Using Miruken Mediator you have the power of a pipeline that runs in any C# application.  This means you can use the same pipeline in Asp.net web apps and web apis, windows services, console applications, WinForms and Wpf applications, WCF, NServicebus, and more.