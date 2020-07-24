---
layout: default
grand_parent: Business Applications
parent: Customer Relationship Management
title: Customizations
nav_order: 7
has_children: true
---

# Customizations
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Considerations before making a change

 It is recommended to use the following approach while adopting a CRM solution:

 1. Use out-of-the-box functionality: In most cases, you will be able to find what you need by using the functionality that is available by default in the CRM solution you bought.

 2. Make configurations: More often than not, as you business grows, so does your CRM. You will find to tweak your objects such as increasing the size of your fields. This can be achieved by making configuration changes to objects.

 3. Creating New Objects: Configuration changes do not permit you to add new objects such as new fields, new menu options or new screens. In these circumstances you will need to create new objects, but this can be done without writing code and by using in built designer tools. 

 4. Developing new scripts: In most of the cases, customizations will not require you to write code. However more complex scenarios such as integrations with 3rd party application will require you to write code to make changes to the way the CRM solution works. This is least recommended scenario.

  ![](assets/images/customizations.png)

## Customizing the Salesforce Platform

Building a new functionality could refer to:

  - customizing existing Salesforce offerings
  - building an app from scratch

The salesforce core platform lets you develop custom data models and applications for desktop and mobile.

Heroku empowers developers  to build highly scalable web apps and back-end services using Python, Ruby, Go. It also provides database tools to sync seamlessly with data from Salesforce.

Salesforce APIs help developers integrate and connect enterprise data, networks, and identity information.

Mobile SDK is a suite of technologies that enables you to build native, HTML5, and hybrid apps that have the same reliability and security as the Salesforce app.

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


 ### Tests and Deployments in Salesforce



## Customizing the Microsoft Dynamics Platform

  ### Tests and Deployments in Dynamics

## Customizations : Dynamics 365 vs Salesforce

### Customizing the Core Product
<br />
**Dynamics 365** can be easily customized for individual needs of customers without the need to rely on third party applications.

Customing the core product in **Saleforce** is limited and way harder.

### Supported Languages 
<br />
**Microsoft Dynamics** supports universal programming languages like Javascript, .NET , Silver Light, and HTML. The Dynamics API also supports a wide variety of methods and functions to integrate with other systems. 

**Salesforce** can only be extended using its own proprietary language called Apex. 

### From the Developer perspective
<br />
**Dynamics 365** allows organizations to personalize, change, and extend the system. Almost every field, dashboard, entity, report, and other aspects of the user interface can be modified at the user level. 
There are also several apps available to extend the functionality of the system. These apps enable users to customize the required objects with little to no coding, in addition to allowing heavily customized apps.

**Salesforce**, offers limited customization options.Salesforce is built on a multi-client cloud environment. Therefore,resources are shared across different organizations, leading to poor performance in comparison with Dynamics.  Your developers can create extra workloads to overcome these limitations which could be cost ineffective and time consuming.


### From the Administrator perspective
<br />
**Dynamics** administrators can manipulate business process workflows to accomodate specific requirements.


### Learning Resources
<br />
There's plenty of ways to learn the platform via Microsoft Learning. The vendor's instructional materials include videos, as well as eLearning and in-person courses leading to role-based certifications. You can also download older Microsoft Dynamics 365 eLearning courses for self-study on the Dynamics Learning Portal.


## Customizing Microsoft Dynamics 365

### User Stories

#### Next Gen Network App

- Application from Ministry of Education 
- Hosted on Dynamics 365 on Azure managed by OCIO
- Not many custom objects have been added to the Application
- Most of the enhancements done were around adding extra security fields, adding security profiles to prevent fields being visible to external vendors as well as hiding implementations details
- A non managed CRM solution is being used mostly in BC Gov. Managed CRM solutions are handy when you are a consulting firm, want to package a CRM solution and sell it to a customer ensuring that they cannot make any changes to the source. The major drawback of a managed solution is that, if there is a need to rollback, it results in data removal.
- There are four environments on which the App is hosted in Dynamics on Azure (Dev, Test, UAT and Prod).
- 95% of the changes were made without making code changes.
- Whenever there is a need to make a change, a blank solution is created, the solution is developed on the Dev environment and the changes are added to the blank solution. The blank solution is downloaded in form of xml files and uploaded to a source control, in this case, SVN. This solution is then released and migrated to UAT and Prod environments using the Dynamics Solution Migration where typically a container is created and changes are deployed to Production.
- Changes can also be made using the Environment Copy approach. But this is not recommended and is only performed when a new App is being deployed to Dynamics, where a copy of the Dev environment is made to production, this could lead to overwriting data in Production, due to which this method is not preferred.
- Dynamics on Cloud is frequently updated and it has been found that the on prem Dynamics is mostly a couple of versions behind the Dynamics on cloud. The application architects, dynamics developers and administrators need to constantly keep themselves up-tp-date with new version upgrades.
- Any new objects created or updated are logged using the object description and other documentation methods. Dynamics offered a space known as Knowledge base articles but it has not been found extremely useful. Adding new objects is relatively simple procedure and you can use the screen to intuitively add names of fields you want create or add.
- Any code changes made have been made by external vendors or contractors and Ministry as well as Microsoft recommends least amount of changes using code. It is encouraged to make configuration changes as much as possible.
- Customizations using Code are mostly required when there need to be third party integrations like integrating with CAS (a Ministry of Finance application). 3rd party integrations are extremely complex with Microsoft Dynamics and it works well as a standalone app. Microsoft Dynamics supports languages such as C, C#, HTML, CSS and JavaScript for making code changes or writing new functionality.


