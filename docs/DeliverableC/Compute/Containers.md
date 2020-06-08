---
layout: default
parent: Compute
title: Containers
nav_order: 3
---


# Containers

  Containers are an evolution of the Virtual Machines. Whilst Virtual Machines themselves being guest machines with operating systems installed that add a significant overhead on the host, containers are small run time environments which share the base operating system kernel which contain just enough resources to run your applications. As defined by Docker, they are isolated from one another, bundle their own software, libraries and configuration files and can communicate with each other using well defined channels. Containers are loosely coupled and short lived and require orchestration platforms to help manage them. 

  Kubernetes is an open source container orchestration platform that helps to automate the deployment of containers, and help manage other aspects such as resource utilization, scaling and load balancing. Though originally designed by google, Kubernetes is now maanaged by Cloud Native Computing Foundation.

  OpenShift Container Platform, an on-premises platform as a service, used widely in the BC Government is built around Docker containers orchestrated and managed by Kubernetes on a foundation of Red Hat Enterprise Linux. Openshift therefore comes with better and more strict security policies than default kubernetes. One of the major advantages of using openshift is it forbids to run the containers as "root" or "super-user" account. This can prevent ad-hoc changes from the development team on production applications, which might be not recorded or applied to the next deployment or might be quick fixes. Openshift locks down this approach and enables the development team to troubleshoot issues and apply long term bug fixes with just a single path to make changes to the production environment which should typically be the CI/CD pipeline.

  Adopting Containers help adopt a DevOps culture within your team and helps to decouple your applications, reduce dependencies, and work towards a domain driven design approach. Containers die easily and can be easily started from the container image built and stored in the platform registry from your application code. This is automatically done by the orchestration platform and so is the sharing and allocation of resources. 

  By using containers, and configuring them for high availability and resilience, you can ensure that, even if 



## Pros

  1. The major benefit of investing in Physical Servers is that they provide you with the ability to manage and configure the components according to your business specifications.
  2. Physical Servers also offer you with the flexibility to decide where to locate them; you can choose to locate them onsite or within a conveniently located facility.

## Cons

  1. The initial cost of ownership and maintenance of Physical Servers is very high. There might be need from time to time to add more resources for scaling your system based on demand, these will lead to evaluation and additional costs required to procure resources. Your application might have a lesser demand from time to time and this might lead to underutilization of resources as well making it hard to scale Physical Servers.

  2. The Physical Server infrastructure should be continuously maintained (24/7 for 365 days in a year) by your in-house employees or with help from external contractors. You would also be responsible to keep your systems up to date, by updating/patching software and hardware constantly and renewing licenses to ensure system security. The updations can lead to considerable downtime of applications as well. 

  3. Setting up your Physical Servers for disaster recovery is highly important and recovery in case of disasters could take hours or days to buy new servers and configure them. For fall back, you might decide to locate a geographically distant datacenter which adds to the initial and maintenance costs.


## The BC Gov Story

   BC Government has two datacenters, one located in Kamloops and the other in Calgary. The one is Calgary is mostly used to host Delivery and Test Environments and the one in Kamloops hosts the production environments.

### Application statistics

| Type of Software category | Application Archetype | Number of Apps on Containers       |
| --------------------------|-----------------------|------------------------------------|
|                           | Call Centre           |                                    |
|                           | Case Management       |                                    |
|                           | Content Management    |                                    |
|                           | CRM                   |                                    |
|                           | Grant Management      |                                    |
|                           | HR                    |                                    |
|                           | Learning              |                                    |
|                           | Licensing             |                                    |
|   Business Applications   | Mapping               |                                    |
|                           | Online Disputes       |                                    |
|                           | Payment               |                                    |
|                           | Portfolio Management  |                                    |
|                           | Registry              |                                    |
|                           | Reporting             |                                    |
|                           | Service Management    |                                    |
|                           | Survey                |                                    |
| Productivity Applications | Office 365            |                                    |     
|                           | Skype                 |                                    |  
|                           | DBMS                  |                                    |
|                           | Middleware            |                                    |
|                           | Search                |                                    |
|    System Applications    | Notification          |                                    |
|                           | Integration           |                                    |
|                           | Accessibility         |                                    |
|                           | Access Management     |                                    |
|                           | Bulk Email            |                                    |


### Applications Archetypes that can be hosted on Container Platforms


### Best Practices to move from Physical Servers to Container Platforms


### Best Practices to move from Virtual Machines to Container Platforms



