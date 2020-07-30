---
layout: default
grand_parent: Business Applications
parent: Product Approach
title: Adopting DevOps
nav_order: 3
---

# Adopting DevOps

## What is DevOps?

Scenario : Your team consists of three developers working on writing new features and fixing bugs in your application. Some of the major challenges the developers might face are:

 1. Time taken for a change to get to production: Owing to manual processes and reviews, a small change or bug fix, might take months to go to production.
 2. Environment Drift: There is a significant difference between the developers local environment and the test and production environments due to which there can be dependency errors and developers can be relieved only once their code is in production. 
 3. Managing a backlog of pending changes and new changes: Due to the delay in pushing changes to production, it becomes difficult to manage the code base comprising of pending changes and new changes waiting in the pipeline. Due to environment drifts, the pending changes might essentially require bug fixes that may affect the new changes the developer needs to make.


 Your team has also has a system administrator who is responsible for managing, monitoring and maintaining the infrastructure on which your application is deployed and ensuring that your application has 99.99% uptime. The major challenges a system administrator face are:
 
 1. Constantly growing infrastructure: The system administrator has to constantly keep pace with the growing number of servers and ensure they are all patched and upgraded. 
 
 2. Solving the environment drift: The sysadmin is responsible for deploying code to production. Due to the environment drift, the code always needs some change before it can actually work on production. The sysadmin therefore needs to take significant time out of their regular work, schedule deployments in advance in order to make these changes. The scheduling in turn affects the time for a change to go to production.

 3. The 2:00 am Calls: The sysadmin is responsible to solve any errors that arise once the code is deployed to the production environment and could get the 2:00 am call in case something goes wrong where in they need to diagnose the logs and fix the issues. More often than not, it might be a fix the developer needs to put in.

**DevOps** is a way in which the **Development** and **Operations** team can work together towards the same goal: Better service for British Columbians. 

By adopting DevOps, both these teams work together and share responsibilities by :

- Automating infrastructure
- Automating the application change and release process
- Continuously monitoring and measuring application performance

By automating the application change and release process, the deployments no longer need to be scheduled and can happen whenever the developer wants to make a change. Typical release cycles remain short between daily releases to bi-weekly releases with the adoption of Agile.

By automating infrastructure, moving to cloud and storing infrastructure as code, the developer can be provided with means to develop code on environments very close to production thereby solving environment drifts. 

Addition of monitoring tools and constantly measuring the performance of the application can help to proactively find potential issues that could arise in future and help mitigate them beforehand.

A typical process for making a new change would a shown below:

!()[assets/images/pipeline.png]

To note:

 - This is one of the few best practices followed
 - The CI pipeline and CI/CD pipeline are not 2 pipelines, it is not good practice to run 2 pipelines from a given repo. The CI pipeline in the same CI/CD pipeline which works differently when the Pull Request is made to a master branch and any other branch.
 - This flow follows a git flow, where the release branch is merged once the change is in production.
 - The pipeline can be run using any orchestrator like Jenkins or Circle CI or Gitlab CI etc.
 - It is considered good practice that the build and deploy should be done within the pipeline using a single commandline which would also work from the developers local machine.
 - Adding manual gates or approval stages in the pipeline would make it Continuous Delivery and a completely automated pipeline is Continuous Deployment. Continuous Delivery is a slow and steady path to move towards the Continuous Deployment Model.

 


References:

[What is DevOps](https://www.youtube.com/watch?v=_I94-tJlovg)
