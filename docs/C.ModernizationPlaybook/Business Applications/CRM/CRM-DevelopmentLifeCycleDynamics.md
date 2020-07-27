---
layout: default
grand_parent: Business Applications
parent: Customer Relationship Management
title: Development Life Cycle in Microsoft Dynamics
nav_order: 9
has_children: true
---

# Development Life Cycle in Microsoft Dynamics
<!---{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc} -->

## Customizing the Salesforce Platform

Building a new functionality could refer to:

  - customizing existing Salesforce offerings
  - building an app from scratch

The **salesforce core platform** lets you develop custom data models and applications for desktop and mobile.

**Heroku** empowers developers  to build highly scalable web apps and back-end services using Python, Ruby, Go. It also provides database tools to sync seamlessly with data from Salesforce.

**Salesforce APIs** help developers integrate and connect enterprise data, networks, and identity information.

**Mobile SDK** is a suite of technologies that enables you to build native, HTML5, and hybrid apps that have the same reliability and security as the Salesforce app.

Developing features on Salesforce can be broadly classified into:

**Declarative Development** : 

Declarative development allows you to develop custom objects and functions specific to your business  without writing a single line of code. You can use forms and drag-and-drop tools to build these custom features.

For example, if you want to add a new custom field, lightning components allows you to do this by using the Object Manager, which has a wide variety of predefined field types to choose from and equips you with a point-and-click development tool kit.

In Salesforce, metadata forms the structure of your instance. It holds configuration such as fields and business processes. If you are developing on the Salesforce platform, it is aware of your metadata and can autogenerate dialogs, record lists, detail views, and forms. It also allows to create, read, update, and delete custom object records in the database.

Some development tasks, like writing validation rules or hooking up components with UI elements, require some basic programmatic knowledge to complete but can be done using the Process Builder by building flow charts.

To summarize, object builder, schema builder and process builder help you develop features without writing code.

**Programmatic Development** : 

Programmatic Development allows you add further extensions, integrations and enhance the functionality of of your CRM.


When there is need to add additional functionality, there are three core programmatic technologies in Salesforce:

 1. **Lightning Component Framework**: A UI development framework similar to AngularJS or React. The Lightning component framework can be used when you want to build a custom user interface. 
 2. **Apex**: Salesforce’s proprietary programming language with Java-like syntax.
 3. **Visualforce**: A markup language that lets you create custom Salesforce pages with code that looks a lot like HTML, and optionally can use a powerful combination of Apex and JavaScript.


## Deploying Changes in Salesforce

 As in the case of any application development, it is not considered good practice to make changes directly to the production environment. It is recommended to have at least 2 other sandbox systems namely dev and test. The developers use the dev sandbox to play with customizations and once they are ready, they are migrated to the test sandbox where there is a user acceptance test done by both the business and quality assurance after which the changes are migrated to Production.

 In the case of salesforce deployments, each sandbox is treated as a separate salesforce org. Whether you are using declarative or programmatic development approaches, you can make customize the salesforce app in five different ways:

 1. Develop and deploy Apex in the Developer Console
 2. Develop and deploy using Salesforce Extensions for Visual Studio Code
 3. Develop and deploy using Metadata API
 4. Deploy using the Ant Migration Tool
 5. Deploy using Change Sets

## Customizing the Microsoft Dynamics Platform

  ### Tests and Deployments in Dynamics

Also Read:
(Customizations: Dynamics vs Salesforce)[CRM-CustomizationsDynamicsvsSalesforce.md]
(Development Life Cycle in Salesforce)[CRM-DevelopmentLifeCycleSalesforce.md]