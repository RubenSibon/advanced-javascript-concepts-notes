# Event Loop, Call Stack en Callback Queue

## Event Loop

Continually checking if the **call stack** is empty. Runs functions and sends calls to the appropriate destinations such as the external Web API.

## Call Stack

*Synchronous* functions get added to the call stack.

## Web API

*Asynchronous* functions like setTimeout use the Web API. Their logic is handled "over there" in a separate thread. They return a **callback** which goes to the **callback queue**.

## Callback Queue

Asynchronous callbacks arrive in the callback queue. They are picked up by the **event loop** and send back to the **call stack** *IF* it is empty and the synchronous functions (i.e. execition contexts) have finished running.
