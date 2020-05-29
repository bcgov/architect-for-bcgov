---
layout: default
title: Cloud Native Principles
parent: A to Z of a Modern Application
nav_order: 2
---


# Cloud Native Application

##  What is a Cloud Native Application
 
   Modernizing application architectures and moving it to the cloud requires that your application is cloud native or a 12-factor application. Being cloud native helps minimize costs and improve agility, resilience, scalability and high availability. The twelve factors that define a cloud native application are listed below:

   1. Every application should have its own code base in a version control system. Cloud Native advocates a single repository, multiple deployments to different environments. 

   2. The application being deployed to will have certain dependencies such as external libraries. These dependencies need to be isolated from the code but needs to  be maintained along with code. No assumption should be made that the environment where you deploy your application will contain these dependencies pre-configured and in case your server fails, or you need to migrate, your deployment to a new environment should contain all dependencies required for your application to work.

   3. Configuration is environment specific items such as database connection strings, usernames, passwords, ssl certificates, ssh keys, environment specific configuration files etc. These configurations should be isolated from code and not stored in the code base. They should be stored securely and fetched during runtime.

   4. Your application will talk to many services such as database, messaging services, email services, caching services etc. Irrespective of where these services are hosted/running, your application should be able to connect to them using a single endpoint (url with/without credentials). Your application should not need to know where these services are running.

   5. The process of packaging your code(build), deploying or releasing the code in different environments and running the application should be isolated from each other and this process should be automated. Ideally, the code should be built once and deployed across multiple environments.

   6. Ideally the application should be stateless and the processes within the application don't share anything with each other implying that there will be no information/log cached in the memory on in the disk for a future request. Anything that needs to persist is stored in the database.

   7. The application should bind its services to ports and listen on those ports to serve requests. It should not become necessary to rely on the runtime injection of a webservice.

   8. To ensure scalability and high availability, the application should be deployed across multiple instances/regions/availability zones instead of increasing the capacity of one instance where the application is deployed. The application should also be split into multiple smaller services.

   9. An application should have minimal start up time, should be able to gracefully shutdown at minimal notice and should have the ability to recover quickly from sudden failures.

   10. The build and release to different environments should happen over multiple stages of an automated pipeline. The various application deployment environments and the process for deployments should be as similar to each other as possible. The time gap between development and production should be reduced to hours/few days from months. The changes/new features should be kept small and the deployments should be more frequent. 

   11. It is important to configuring logging for the application as well as the backend pieces such as the database. Logs help developers understand and debug reasons for failures as well as predict and fix future failures. Logging mechanisms should be configured such that the information is output as a continuous stream and published using appropriate tools. Logs should be continuously rotated and archived using automation.

   12. Applications would require one-off processes such as batch scripts and database migrations. These processes should follow the same standards as the application, they should be in version control, and also follow the same deployment process along an automated pipeline through similar stages.


## What would happen if an application that doesn’t follow the 12 factor rules is deployed to cloud?

1. **What if there is no code base in a version control system?** 

    If there is no version control system, in a situation in which you deploy a new version and it fails, it would be difficult to revert back to a previous version as well there would be no tool using which your developers would be able to continuously integrate their changes. A distribute version control system like Git (Bitbucket, GitHub, GitLab) is preferred over a centralized version control system such as Subversion (or SVN), to enable developers to have their own local copy of the repository, work simultaneously and integrate the components they work on, with ease. 
    
    A centralized version control in contrast would place locks on files being edited and changes can only be submitted one at a time. Git also provides functionality to easily incorporate DevOps practices and add automation.
    
    There should also be one code base for each application or for each application component (microservice) to ensure they are all properly versioned separately.


2. **What if the application dependencies are not maintained along with the code base?**

    It is extremely important to isolate and maintain/declare the application dependencies along with the code base, for instance, you might be deploying to a new environment which doesn’t contain the libraries/packages your application needs due to which your application will fail to load. 

    Therefore, fetching these dependencies and packaging them along with your application will help you deploy your application to any platform and can also be migrated easily without having the need to preconfigure the environment you deploy to.


3. **Why should the configuration items be separated from the codebase and fetched during runtime?**

    Configuration items include passwords, ssh keys, ssl certificates, database connection strings etc. These are generally environment specific, they are highly sensitive and/or might change frequently. It is therefore essential to store them separate from the code base which is accessed by multiple people and fetched at run time.

    By parameterizing your code base and making sure there are no environment specific configurations within your code base, it becomes flexible to run your code in any environment and can be easily migrated to a different environment when needed. This also helps restrict data and allow developers to know only what they need to know.

4. **Why should the application be agnostic of where the backing services are hosted?**

    If your application is aware and relies on where your database, messaging, or any other backing service is running, if there is a failure in any of these backing services and there is a need to spin up new servers, the application would need to be changed significantly. If the application is not aware of where these services are hosted and connects to these services using a url and credentials, even if a new instance where these services are hosted is spun up or if these services are migrated, there will be minimal/no impact on the application.

5. **Why should the build, release and run processes be separated and automated?**

    Separating the build process from the release and run process ensures, changes are not made during runtime. If changes are made during runtime, there is a chance that these changes might not be incorporated the next time the application is deployed or when the instance restarts. The developer puts in all the changes in the code base, creates a portable build artifact during the build stage which is released and run across multiple environments. This will also help setup appropriate gates prior to release and run in each environment to include quality assurance and user acceptance.

6. **What would happen if an application is stateful?**

    If you have multiple instances across which the application load is balanced, and if your application is stateful, if one of the instance fail due to any reason and the workloads on that instance switch over to another, it could result in failure or loss of information since the previous state would be lost.
      
    Therefore, it is recommended practise to ensure that your application is stateless.

   
7. **What is the need to configure port binding?**

    Port binding ensures that each micro service within the application is self-contained with ports they serve stored as config enabling them to talk each other using the specified ports.


8. **Why do we need to stop scaling vertically and start scaling applications horizontally?**

    Vertical scaling also known as scaling-up, implies adding more computation power (CPU,RAM) to the instance/server on which the application is deployed to meet the growing demand.

    Horizontal scaling, also known as scaling-out, on the other hand implies adding more instances or more application deployments into the pool of resources.

    The major disadvantage of scaling-up or vertical scaling is that, you impose on yourself the need to keep adding resources as the demand grows and there will be a limit up to which this can be added. Adding more resources or using resource intensive machines on the cloud will prove to be more expensive and these resources might be under-utilized when the demand is less. Also, if the server goes down, the application goes down along with. 

    In contrast, if horizontal scaling is used, you can use minimal resource configuration, thereby paying a lower cost, but investing in multiple instances of the same type. By utilizing features provided by various cloud providers, you can host the application on instances spread across multiple regions, thereby ensuring, even if one region is down, your application remains accessible via the other instances that are up. Using autoscaling options, you can easily set the threshold and decide when and how many instances you need at a particular instance of time based on the demand.


9. **Why is application disposability important?**

    It is highly important to make your environment disposable to ensure its fault tolerant. If your application or the instance on which your application is hosted goes down, it should be easy enough to bring it up within minimal time. This would imply that application, the infrastructure, and other components such as storage, network and database should all be stored in the form of code from which they can be recovered in case of any accidental deletion or unforeseen failures.

    Similarly, when processes terminate, they should finish their current request, refuse any incoming request, and then terminate.


10. **What would happen if the development and production environments are not similar to each other?**

    If there is parity between the development and production environments, there is possibility of incompatibility and what might seem to work in a developer’s local environment or in the development or staging environment might fail when it is deployed and released to production. By ensuring all environments are similar to each other and kept as close to production as possible, it would be easier for the developer to develop compatible code and debug issues in the earlier stages.
   
    This also implies making sure that the deployment processes are simple, are a single command line and there are transient production-like environments configured using code so that developers can deploy locally and debug their changes. It is also important to ensure your automation is not dependent/specific to any tool. It should be able to work from any environment.

    This would help in building a reusable, fully automated, portable continuous delivery pipeline.


11. **What happens if logs are not configured?**

    If your application logs are not configured extensively, it will difficult to determine the root cause in case of any failures. The logs should be stored within a persistent storage outside the easily destructible cloud instances to ensure they are available all the time. By storing logs in files of specific formats, monitoring and visualization tools can be used to parse these logs and raise alerts when something goes wrong or even predict if something could go wrong within your system.


12. **What is the importance of treating one-off processes just like application code?**

    It is important to treat one-off processes such as batch jobs and database migrations follow the same standards as the application, they should be in version control, and also follow the same deployment process along an automated pipeline through similar stages.

    For instance, if database migrations are version controlled and scripts migrated via an automated pipeline using tools such as Liquibase, Flyway DB etc., it will help to make the migrations repeatable. These tools manage the versions using a changelog and only apply changes that have not been applied. This will help applying small changes faster and more frequently and also enable provisions to add recovery scripts.

     

     










   



