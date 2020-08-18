---
layout: default
title: Monoliths vs Microservices
parent: Domain Driven Design
grand_parent: Modernization Playbook  
nav_order: 1
---

# Monoliths vs Microservices

## Am I working with a Monolith?

<img src="assets/images/quote4.png">

 A monolithic software application is defined as a single-tiered application in which the different components of the architecture such as, business logic, user interface, database layer , application integration, authorization etc are all combined into the same program. 

 Is your application code base large and contain the code for the front end, backend, data access layer and database scripts within the same repository? If yes, you are working with a monolith.

 Are your application components tightly coupled with each other in such a way that, if you want to make some database changes, you need to deploy other components, or if you want to deploy a change to the frontend, there would be a database migration in effect? If yes, you are working with a monolith.

 Are there too many application dependencies, that make frequent changes to components a distant dream and it takes more than a few weeks to deploy a change to your application and also maintaining each component is extremely hard? If yes, you are working with a monolith.

## What are microservices? 

  Microservices are small, autonomous, decentralized, self-contained pieces of business functionality that can be independently deployed. Microservices should typically be the size of a class in terms of object oriented programming language, or basically a few lines of code. The implementation details of microservices should be hidden from each other in order to ensure they are decoupled and autonomous.

  Microservices need to be designed and Domain Driven Design is one of the ideal ways to design microservices. 


## How do I choose between a monolith or a microservice?

  The ability of microservices to be independently deployed indicates that deploying a component of your architecture will not affect the whole system. If you dont want independently deployable components, you need to choose working with a monolithic architecture.

#### **Advantages of Monolithic Architecture**:

  * Simple to develop with a single code base.
  * Easy to test.
  * Scale horizontally behind a single load balancer.

#### **Disadvantages of Monolithic Architecture**:

  * Simplicity is inversely related to the size and complexity. As the application grows, the monolithic architecture becomes more complex.
  * The size of a monolith is large which tends to have slower start-up and built times
  * Change to a small components affects the entire system
  * Adopting a DevOps Culture as well as new technologies is difficult
  * Low reliability
 
  In scenarios where there are a huge number of dependencies and your application is being deployed to cloud, it becomes harder to make small changes without having to rebuilt and redeploy your entire system which might take days of effort and becomes hard to maintain over time. When it comes to scaling resources, you might need to scale resources for your entire application rather than scaling it only for the component that requires additional resources thereby incurring more costs.

#### **Advantages of Microservices**

 * Improved fault isolation.
 * No vendor or technology lock-in.
 * Easy to understand.
 * Smaller, faster and frequent deployments.
 * High Scalability.

#### **Disadvantages of Microservices**

 * Testing a microservices application is complex since it involves several components.
 * Heavily relies on automation and training of employees in latest technology trends.

