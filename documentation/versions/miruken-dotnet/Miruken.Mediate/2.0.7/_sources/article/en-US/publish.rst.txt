=======
Publish
=======

:code:`Publish()` is an :code:`IHandler` extension method that is used for notification.  It will traverse the context and execute every handler that can handle the message. If no handler is found, it *will not throw* and exception.  Published messages do not return a response.

In this example we are executing :code:`Publish()` off of the :code:`IHandler composer` that is passed in to the :code:`[Mediates]` method.  Mediator will find and execute all handlers that can handle TeamCreated.

.. literalinclude:: ../../examples/handler/withComposer/teamHandler.cs
