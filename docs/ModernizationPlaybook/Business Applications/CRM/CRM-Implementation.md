---
layout: default
grand_parent: Business Applications
parent: Customer Relationship Management
title: Implementing CRM
nav_order: 7
---

# Implementing CRM

### On Premise
 
One of the options for implementing a solution is building a custom one.
 
#### Pros
 
  1. Ability to customize and build features that are essential to your organization
  2. Complete control on your systems and data
 
#### Cons
 
  1. You need to set up an agile team to iteratively develop and manage the custom build solution
  2. The time and cost taken to custom build a CRM solution are on the higher side
  3. You might end up reinventing the wheel
 

### Cloud
 
  According to a study by IBM, 88% of CRM solutions were on premise and custom built in 2008 whereas 87% are cloud based today. By choosing to move towards a Cloud CRM or SaaS solution, you are relieved of installing, configuring and maintaining your own servers and infrastructure for the CRM solution. You only pay for the licenses per the number of users.
 
#### Pros
 
1. Lower upfront cost
 2. The installation, maintenance, upgrades, back-ups, integration and resolution of technical issues are all managed by the vendor.
3. Quicker deployment process.
4. Flexibility of payment – you can increase or decrease subscriptions as and when required.
 
#### Cons
 
1. Possible vendor lock-in
 

## Salesforce

Salesforce is a cloud based Software as a Service (SaaS) where the software is delivered to the end user via the Internet. The usage of Salesforce is therefore subscription based. As a Salesforce customer, there will never arise a need for procuring infrastructure resources (Compute, Storage and Network) to host your CRM app. The infrastructure management and maintenance, software patches and upgrades, advanced security measures, scaling infrastructure based on demand are all offloaded from customer end and are completely managed by Salesforce. 

Salesforce also offers a Platform as a Service (PaaS) product by the name of Salesforce Platform which provides various tools such as Lightning App Builder, Heroku enterprise etch which can be used for building an application from Scratch.


The cloud platform offers great integrations with code editors such as VSCode, version control systems such as Git, as well as Build and Deployment Orchestrators such as Jenkins for establishing an automated Change Release pipeline.

## Microsoft Dynamics 365

Dynamics 365 can be implemented in three ways:

1. **On Premises**: In this method, the customer is responsible for managing and maintaining the infrastructure, upgrading and applying patches, managing data storage as well as ensuring security. This method could lead to high upfront costs. The on premise option might seem viable in the following situations:

  - For organizations transitioning from small to medium, which do not have enough bandwidth to keep up with changes or make new customizations and configurations frequently.

  - For organizations that have a stringent security policy around their data and want to prevent any external access via the Internet to their CRM application.

  - For a very specialized application, which has come out of a lot of customizations over the out of the boz product which might not be able to sustain in a cloud environment that is constantly changing and updated with new features.

  - When large amounts of data need to be pushed back and forth between systems, such as fraud detection systems, it would be more viable and fast to host an on premise solution within the same network.

2. **Dynamics Online**: Dynamics Online is a cloud based SaaS offered by Microsoft which works on a subscription model. With this method, you will no longer manage or maintain the underlying IT infrastructure and there will be no locally hosted Dynamics instance in your environment.

Using this option, you can set up your application very quickly and leverage the latest features pushed out by Microsoft regularly. These features can sometimes save you customization efforts.

3. **Hybrid Solution**: In this method, you buy an on-premise software and host it by paying a cloud service provider such as Azure, AWS or GCP. Using this method, you can be in-control of the underlying infrastructure, you can manage and maintain the underlying components, be in control of software updates as well as be wary of where the data is stored. In addition you can take advantage of cloud services and adopt DevOps practices.

## References
* [5 characteristics of a good CRM system](https://sugester.com/article/crm-1)

* [Top CRM Features and Functionality List](https://www.selecthub.com/customer-relationship-management/crm-features-functionality-list/)

* [Salesforce Implementation](https://www.salesforce.com/ca/cloud-computing/)

* [Dynamics Hybrid Deployment](https://thatcrm.com/2018/02/21/is-there-such-a-thing-as-hybrid-deployment-for-dynamics-365-customer-engagement/)

* [CRM Deployment Methods](https://crmbook.powerobjects.com/crmbook-2/choosing-a-deployment/) 