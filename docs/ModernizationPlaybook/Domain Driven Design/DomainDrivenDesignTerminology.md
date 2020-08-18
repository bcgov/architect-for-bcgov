---
layout: default
title: Important Terminology
grand_parent: Modernization Playbook
parent: Domain Driven Design 
nav_order: 3
---


# Important Terminology 

Scenario: 

## Domain 

 Domain is the business area to which the user applies the program.
 
## Bounded Context

Bounded Context is a semantic contexual boundary within which each software component has a specific meaning and a specific function. It is a natural division within the business. For eg: for a book store, there are two contexts, the book store and the warehouse itself.

Responsibilities of people working in each context are different and they work without knowing what people in the other context are doing. Most of the communication happens within each independent bounded context. There would typically be just one object that communicated with another context to make the system work.

### Rules of Bounded Context

1. One team should be assigned to work on one Bounded Context.
2. One team could possibly work on multiple Bounded Contexts but multiple teams must not work on a single Bounded Context.
3. The source code repository and database schema is kept separate for each Bounded Context.

## Entity

 An Entity is an individual or an object within a bounded context. Every entity should be associated with one bounded context.  It is considered bad practice to use one product component in multiple contexts. If there are entities with the same name, different functions within different contexts, they shouldn't be grouped together.


## Ubiquitous Language

The language used within each Bounded Context to build a functioning software model is known as the Ubiquitous Language. Ubiquitous language is both spoken by team members working within the Bounded Context as well as implemented within the software model.

### Rules of Ubiquitous Language

1. People within each context use a language of their own
2. Language of one context differs from the language of other contexts
3. Distinguish between the roles and actors and identify roles while coming up with the ubiquitous language. 
4. Each entity corresponds to the role taken up by actors.





