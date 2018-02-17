=======
Handler
=======

To handle requests create a class that extends from :code:`Handler`.  Then create a method on that class with the :code:`[Mediates]` attribute that takes the request object as the first parameter and returns the response object.

For example, here in TeamHandler.cs we have a method called CreateTeam that takes in a CreateTeam object and returns a TeamResult.  

.. literalinclude:: /example/handler/withHandlerBaseClass/teamHandler.cs

It is optimal that your handler classes inherit from :code:`Handler` but it is not required.  If they do not inherit from :code:`Handler` or implement :code:`IHandler`, Miruken will wrap them in a handler inside the framwork.   

.. literalinclude:: /example/handler/withoutInheritance/teamHandler.cs

Optionally, the :code:`[Mediates]` method can take an :code:`IHandler` as the second parameter.  We call this the composer. The composer is for code composition. Use it within your method to send other messages or publish notifications.

.. literalinclude:: /example/handler/withComposer/teamHandler.cs

