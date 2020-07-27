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

### Change Migration Process for Microsoft Dynamics 365 on Azure offered by OCIO

- There are four environments on which the App is hosted in Dynamics on Azure (Dev, Test, UAT and Prod).
- 95% of the changes were made without making code changes.
- Whenever there is a need to make a change, a blank solution is created, the solution is developed on the Dev environment and the changes are added to the blank solution. The blank solution is downloaded in form of xml files and uploaded to a source control, in this case, SVN. This solution is then released and migrated to UAT and Prod environments using the Dynamics Solution Migration where typically a container is created and changes are deployed to Production.
- Changes can also be made using the Environment Copy approach. But this is not recommended and is only performed when a new App is being deployed to Dynamics, where a copy of the Dev environment is made to production, this could lead to overwriting data in Production, due to which this method is not preferred.
- Dynamics on Cloud is frequently updated and it has been found that the on prem Dynamics is mostly a couple of versions behind the Dynamics on cloud. The application architects, dynamics developers and administrators need to constantly keep themselves up-tp-date with new version upgrades.
- Any new objects created or updated are logged using the object description and other documentation methods. Dynamics offered a space known as Knowledge base articles but it has not been found extremely useful. Adding new objects is relatively simple procedure and you can use the screen to intuitively add names of fields you want create or add.
- Any code changes made have been made by external vendors or contractors and Ministry as well as Microsoft recommends least amount of changes using code. It is encouraged to make configuration changes as much as possible.
- Customizations using Code are mostly required when there need to be third party integrations like integrating with CAS (a Ministry of Finance application). 3rd party integrations are extremely complex with Microsoft Dynamics and it works well as a standalone app. Microsoft Dynamics supports languages such as C, C#, HTML, CSS and JavaScript for making code changes or writing new functionality.


Also Read:
<br />
[Customizations: Dynamics vs Salesforce](CRM-CustomizationsDynamicsvsSalesforce.html)
<br />
[Development Life Cycle in Salesforce](CRM-DevelopmentLifeCycleSalesforce.html)
