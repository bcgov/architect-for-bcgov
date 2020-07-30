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


## Customizing the Microsoft Dynamics Platform

Customizations on the Dynamics Platform can include creating or tweaking custom objects without using code or developing new solutions using code. While developing solutions, you may will need to move your solution from development environment to test environment and user acceptance testing (UAT) environments before deploying it in production.

In dynamics, *solutions* are units of software that developers create, package, and maintain to extend their existing platform.  Multiple solutions are created  when developers are working on components that are totally unrelated to each other.

The different types of **solution components** are:

 - **Schema**: Entities, Attributes, Relationships, Global Option Sets
 - **User Interface**: Application Ribbon, SiteMap, Forms, Entity Ribbons, Web Resources
 - **Analytics**: Dashboards, Reports, Visualizations
 - **Process** : Dialog and Workflow Processes, Plugins
 - **Templates**: Mail-Merge, Email, Contract, Article
 - **Security**: Security Roles, Field Level Security

Different types of **solution** in Dynamics include:

1. **System Solution**: The predefined solution components that define the default application behavior.

2. **Managed Solution**: Managed Solutions (third party software) are installed on top of System Solutions and can add a new solution component or modify a customizable solution component.

3. **Unmanaged Solution**: Unmanaged Solutions can be used to extend or modify System Solutions and Managed Solutions. 


Some of the strategies for customizations include:

1. Multiple developers work on a single dev sandbox or organization ensuring the fact that they work on separate components and that the shared libraries are pre-installed.

2. Within one organization, each developer creates their own unmanaged solution. Each solution components exists only within one unmanaged solution. The unmanaged solution is a subset of the master solution but doesn't contain the existing solution thereby creating a clear boundary between the existing solutions and the solutions being modified.

3. Each developer works on their own organization. Each developer creates and unmanaged solution and it is imported into the master solution.

### Deploying a Solution in Dynamics
 
 - Developers start by creating a blank unmanaged solution in their respective dev organization and start adding solution components to it.
 - Once the development is complete, the developers export the solution and import it into the Test Organization. 
 - The solution files are placed in source control as zip files.
 - The SolutionPackager tool is then used to extract the exported solutions files from source control into UAT and subsequently the Production Org.


Also Read:
<br />
[Customizations: Dynamics vs Salesforce](CRM-CustomizationsDynamicsvsSalesforce.html)
<br />
[Development Life Cycle in Salesforce](CRM-DevelopmentLifeCycleSalesforce.html)


References:

[Dynamics 365 Developer Guide](https://docs.microsoft.com/en-us/dynamics365/customerengagement/on-premises/developer/introduction-solutions)