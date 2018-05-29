====================
Request And Response
====================

Create request and response objects. By inheriting from :code:`IRequest<TResponse>` mediator will know the type of object being returned.

.. literalinclude:: ../../example.league.api/team/createTeam.cs

.. literalinclude:: ../../example.league.api/team/teamResult.cs

:code:`IRequest<TResponse>` is optional.  Mediator will still handle your request without it, but you will have to specify the return type when sending the message.

.. literalinclude:: ../../examples/withPureClasses/createTeam.cs

Responses are also optional.  You can send requests that have no response.
