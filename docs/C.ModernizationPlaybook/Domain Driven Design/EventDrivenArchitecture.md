---
layout: default
title: Event Driven Architectures
parent: Domain Driven Design 
nav_order: 3
---

# Event Driven Architectures

## Deciding if your application can be Event Driven

Event Driven Architecture is best suited for:

 1. Asynchronous Systems with an asynchronous flow of data:  Syncronous systems can be made asynchronous using messaging queues.

 2. UI driven applications: For e.g., In applications that implement search, instead of having a server that is always running, a function can be implemented that responds to HTTP requests via an API gateway and reads from the database on demand.

 3. Message Driven Applications: For e.g., A user centric application that redirects user requests as well as captures and logs the users activity such as a online advertisement system or a recommender system which has a lot of backend data processing. 

 5. Event Driven Architectures using FaaS work well for high volume transactions, workloads that only happen every so often for eg: generating reports, image processing, or any scheduled tasks. 
 
 6. Event Driven Architectures using Containers are seen as a better choice for synchronous, request–driven applications with multiple entry points.

 7. IoT applications

## Considerations for choosing an Event Driven Architecture:

 1. Agility: Within an Event Driven Architecture, components are loosely coupled,therefore, changes made to one component will not affect other components, thereby making frequent and continuous changes possible.

 2. Performance: Event Driven Architectures are ideal for parallel operation of Asynchronous events leading to a better performance.

 3. Scalability: Due to highly decoupled components, Event Driven Architectures scale well to large demand.

 4. Ease of Development: It is considered not that simple to develop an Event Driven Application due to its asynchronous pattern.

 5. Testability: Testing components within an Event Driven Architecture is not simple since it would require special testing tools to mock the combination of events of and sequences.

 6. Durability of your event source: Your event source should be reliable and guarantee delivery if you need to process every single event. 

 7. Performance control requirements: Your application should be able to handle the asynchronous nature of event routers. 

 8. Event flow tracking: Event flows or streams are difficult to track making it hard for developers to find the root cause of a bug or a performance bottleneck.

 9. Data in your event source: If you need to rebuild state, your event source should be deduplicated and ordered.



