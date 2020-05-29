---
layout: default
title: Introduction
parent: A to Z of a Modern Application
nav_order: 1
---

# Introduction to a Modern Application

  Application Development has evolved greatly over the years. A true modern application is developer oriented, decoupled, reliable, highly available, secure and scalable, and should obey the Cloud Native or 12 factor application principles (see also, [Cloud Native Principles](CloudNativePrinciples.md)).


  An application is said to be **developer-oriented** if the developer is not bound by infrastructure requirements. The developers should be able to develop code and run a single command in his local environment which runs tests, and brings up the application with the current changes, including the connections to the other components such as storage and the database. Within this system, setting up development environments with significant effort to run the application and all supporting components, are considered as a hindrance to productivity. The developer environment should also be as close to the actual environment (Production Environment) as it can be for earlier detection of possible bugs and defects.

  An application should be **loosely coupled** or **decoupled** into multiple **microservices** which communicate with each other using RESTful APIs. The application should also support multiple clients and should not be dependent on what UI the client uses or on the number of clients consuming its data and services. Decoupling the applications allows developers to work with smaller pieces and smaller code bases thereby reducing complexity and making it easier to push changes, add innovation, design, secure, manage and maintain each component.

  A modern application should be **highly-available** and **reliable**. High Availability is measured as the amount of time the application is up and available to serve requests to the end users. Most modern applications have an availability of 99.9999% (also known as 4 9s) which mean that the application can be down for around 31s in a year. 

  A modern application is **secure**. It doesnt store credentials in the code base. All required credentials are stored in a secured location such as vaults and are fetched during run time. The system also makes it unneccessary for developers to know credentials and trusts the automation to fetch it correctly. The application is hosted on a secure infrastructure which opens access only to necessary ports and serves applications via HTTPs. All connections within the application components and outside are secure and encrypted. It obeys the **ZERO TRUST** policy and denies all connectivity at first and authentication and authorization is required to gain the necessary access.

  A modern application is also **scalable**. The application utilizes resources based on demand.

   

   


  