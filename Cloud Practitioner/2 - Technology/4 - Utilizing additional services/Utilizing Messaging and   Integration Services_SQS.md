###### Loose Coupling

- Coupling defines the interdependencies or connections between components of a system. Loose coupling helps reduce the risk of cascading failures between components.

##### Loose Coupling

Loosely coupled components are connected but not dependent on each other.

> [!example]
>  micro services

VS

##### Tight Coupling

Tightly coupled components are highly dependent on each other.

> [!example]
> Monolithic Applications

Queues are used to implement loosely coupled systems

# Simple Queue Service (SQS)

SQS is a message queuing service that allows you to build loosely coupled systems.
- Messages are processed in an asynchronous manner
- Allows component-to-component communication using messages
- Multiple components (or producers) can add messages to the queue

## SQS in the Real World

Build a money transfer app that performs well under heavy load.
- SQS lets you build an app that is loosely coupled, allowing components to send, store, and receive messages. The use of a messaging queue helps to improve performance and scalability.