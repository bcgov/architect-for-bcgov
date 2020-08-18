---
layout: default
grand_parent: Modernization Playbook
parent: Compute
grand_parent: Modernization Playbook 
title: Containers
nav_order: 3
---


# Containers

  Containers are an evolution of the Virtual Machines. Whilst Virtual Machines themselves being guest machines with operating systems installed that add a significant overhead on the host, containers are small run time environments which share the base operating system kernel which contain just enough resources to run your applications. As defined by Docker, they are isolated from one another, bundle their own software, libraries and configuration files and can communicate with each other using well defined channels. Containers are loosely coupled and short lived and require orchestration platforms to help manage them. 

  Container Orchestration Platforms help in creating clusters of resource pools or nodes and enabling to share resources among the nodes belonging within a cluster. These nodes can be physical servers or virtual machines. The Openshift Platform set up by BC Gov uses around 20 nodes which are virtual machines hosted in the on prem data center. There is also work being done in hosting these nodes on Azure Virtual Machines.

  Kubernetes is an open source container orchestration platform that helps to automate the deployment of containers, and help manage other aspects such as resource utilization, scaling and load balancing. Though originally designed by google, Kubernetes is now managed by Cloud Native Computing Foundation.

  OpenShift Container Platform, an on-premises platform as a service, used widely in the BC Government is built around Docker containers orchestrated and managed by Kubernetes on a foundation of Red Hat Enterprise Linux. Openshift therefore comes with better and more strict security policies than default kubernetes. One of the major advantages of using openshift is it forbids to run the containers as "root" or "super-user" account. This can prevent ad-hoc changes from the development team on production applications, which might be not recorded or applied to the next deployment or might be quick fixes. Openshift locks down this approach and enables the development team to troubleshoot issues and apply long term bug fixes with just a single path to make changes to the production environment which should typically be the CI/CD pipeline.

  Adopting Containers help adopt a DevOps culture within your team and helps to decouple your applications, reduce dependencies, and work towards a domain driven design approach. Containers die easily and can be easily started from the container image built and stored in the platform registry from your application code. This is automatically done by the orchestration platform and so is the sharing and allocation of resources. 

  By using containers, and configuring them for high availability and resilience, you can ensure that, even if the node on which the container lives crashes, the replicas on other nodes remain unaffected. It has been found that the overall cluster availability was 99.99% for the BC Gov Openshift Cluster even though individual node availability has been around 80%.

[Virtual Machines vs Containers](assets/VMVsContainers.xlsx)

## Pros

  1. Containers are light weight utilize minimal hardware resources in comparison to Virtual Machines and Physical Servers. While Virtual Machines might need 1GB of RAM or 2 CPU cores, a container might just require 512 MB of RAM and 500 millicores of CPU to run the same application.
  2. Applications deployed in containers are highly portable and can be deployed easily to different operating systems or hardware platforms. They also encoourage the development team to build deployment scripts that are cross platform and can be run from any CI/CD orchestrator or even from the developers local machine which reduces platform dependencies and vendor lock-in. Containers are stored as images and containers that run in Openshift can be run on AWS, GCP or Azure without making any changes to them.
  3. Containers are highly efficient and can be quickly deployed. This promotes agility and enables developers to push small changes to components without effecting other components more frequently.
  4. Containers ensure consistency and ensure the development, test and production environments remain the same, since the images are build once and deployed multiple times to different environments. This helps developers to detect failures faster and debug them before they can even be deployed to Production.


## Cons

  1. Despite most orchestration platforms being PaaS, deploying containers still require steps such as choosing the right base image, ensuring the base images are up to date and provisioning other surrounding objects to run the containers such as deployment configurations, build configurations, image streams, services, routes, storage, stateful sets etc. These objects are specific to the different vendors. 

  2. Persistent data storage is a complicated subject with respect to containers and if you have applications that access network shares like Windows Shares, NFS, FTP etc, it becomes increasingly complicated to lift and shift your application unless you design ways to move your data to the cloud.
  
  3. Only applications that are designed to run as a set of discreet microservices stand to gain the most from containers


## The BC Gov Story

  There are several applications being deployed in containers, as well as work is underway on moving applications from legacy systems to the Openshift Platform.

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
|                           | Search                |                                    |
| Productivity Applications | Office 365            |                                    |     
|                           | Skype                 |                                    |  
|                           | DBMS                  |                                    |
|                           | Middleware            |                                    |
|                           |              |                                    |
|    System Applications    | Notification          |                                    |
|                           | Integration           |                                    |
|                           | Accessibility         |                                    |
|                           | Access Management     |                                    |
|                           | Bulk Email            |                                    |


### Applications Archetypes that can be hosted on Container Platforms



### Best Practices to move from Physical Servers to Container Platforms


### Best Practices to move from Virtual Machines to Container Platforms



