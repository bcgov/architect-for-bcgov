---
layout: default
parent: Compute
title: Physical Servers
nav_order: 1
---


# Physical Servers

  The evolution of compute began with using Physical Servers for hosting applications. A physical server is a larger, powerful version of a desktop computer and is housed in a data center. 

  Physical Servers run operating systems and other software applications which utilize the servers hardware capacity such a CPU, RAM, Storage and network devices. Physical servers do not typically share resources with each other in a data center thereby limiting the number of applications that can be housed on them.

## Pros

  1. The major benefit of investing in Physical Servers is that they provide you with the ability to manage and configure the components according to your business specifications.
  2. Physical Servers also offer you with the flexibility to decide where to locate them; you can choose to locate them onsite or within a conveniently located facility.

## Cons

  1. The initial cost of ownership and maintenance of Physical Servers is very high. There might be need from time to time to add more resources for scaling your system based on demand, these will lead to evaluation and additional costs required to procure resources. Your application might have a lesser demand from time to time and this might lead to underutilization of resources as well making it hard to scale Physical Servers.

  2. The Physical Server infrastructure should be continuously maintained (24/7 for 365 days in a year) by your in-house employees or with help from external contractors. If a server goes out of date, all applications running on it are at risk  You would also be responsible to keep your systems up to date, by updating/patching software and hardware constantly and renewing licenses to ensure system security. The updations can lead to considerable downtime of applications as well. 

  3. Setting up your Physical Servers for disaster recovery is highly important and recovery in case of disasters could take hours or days to buy new servers and configure them. For fall back, you might decide to locate a geographically distant datacenter which adds to the initial and maintenance costs.

  4. Each Application is normally deployed (resides) on three servers or environments. Typically, these environments are known as development, test and production. The development (dev/dlvr/int) environment is typically where developers do their development. The test environment is where the code changes/application changes are tested by the business. The production environment makes the service available to end users. It is common in traditional infrastructure to maintain development, test and production environments slightly different owing to repetitive manual configurations and reduce costs. This would result in configuration drifts between these environments which can lead to bugs or defects in the application in production which do not surface during testing or development


## The BC Gov Story

   BC Government has two datacenters, one located in Kamloops and the other in Calgary. The one is Calgary is mostly used to host Delivery and Test Environments and the one in Kamloops hosts the production environments.

### Physical Server Types

### Application statistics

| Type of Software category | Application Archetype | Number of Apps on Physical Servers |
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


### Applications Archtypes worth keeping on Physical Servers
                            

