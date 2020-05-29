---
layout: default
title: Lift and Shift Strategies
parent: How-to-Guides
has_children: true
nav_order: 1
---

## A guide to lifting and shifting your Legacy Application to Cloud

Cloud provides you with an excting range of opportunities to add innovation to your application using which you can provide better service to your end users. From being able to make changes faster to not being responsible for managing the infrastructure, Cloud would definitely add value and increase agility.

Before you move to the cloud, it is important to understand the definition of a legacy application.

* A legacy application is monolithic or has several components tied within a single unit.
* A legacy application can have multiple dependencies on other applications or data components, thereby making changes are highly complicated
* A legacy application could either be hosted on an on prem datacenter or on a single physical server behind someones desk.
* A legacy application could also be hosted on a virtual machine in an on prem cloud but is significantly old, out of date and out of warranty.
* A legacy application cannot be dynamically changed, it might take months of effort to make a small change and might be cost intensive.
* If you need to think twice before you push a new feature or change, notify your end users the application will be going down more frequently than 30s yearly, and falls under any of the above mentioned category, it can be classified as a legacy application.

## Strategies for lifting and shifting
When you decide to move your legacy application to the cloud, there are 6 strategies you can adopt, that are also knows as Gartners 6R's.

**Rehosting or Lift and Shift**: In this approach, you would typically run your application on the cloud making minimal changes. You might even choose to leave your database behind in the interest of not making changes to your application. Once your application is running on the cloud platform of your choice, you will then work on optimizing your application.

**Replatforming**: If you are adopting this approach, you would need to make some changes to your application in order to take advantage of equivalent services offered on the cloud. You will first be required to evaluate the different cloud services and change your application and database components to suit the needs of the services that you choose to replatform.

**Repurchasing**: This approach is applicable when you want to move to SaaS. You have an in-house application, but you decide, there is better equivalent in the market. You can purchase and use this product, without needing to host it on your infrastructure, thereby saving costs and other resources.

**Refactoring/Rearchitecting**: This approach can be adopted when you want to go towards microservice oriented architecture or even serverless. You will need to decouple and rewrite your applications, write APIs, rearchitect your application and infrastructure and then integrate the changes into cloud. This might have high initial costs, but will prove to be the most benefitial approach in the long run.

**Retiring**: When you are thinking of moving to the cloud, it is important to ask the question, do I really need this application any longer. It might be time for you to determine and analyze, if there are other newer applications that render similar functionality and also determine how often and how many people actually access the application. If the application is being hardly used by 1 or 2 users in a week and a change is made to it once in a year, that application can be got rid off instead of wasting cost and effort required to host in on cloud.

**Retaining**: You will use this approach when you might have recently spend cost and time to upgrade your application but you are not inclined towards moving it to cloud right away. You cn then choose to retain the application as it is in the current infrastructure and state.

