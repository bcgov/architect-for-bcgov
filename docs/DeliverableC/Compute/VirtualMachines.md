---
layout: default
parent: Compute
title: Virtual Machines
nav_order: 2
---


# Virtual  Machines

  To overcome issues with physical hardware, the concept of virtual servers was introduced.  Virtualization is the process of running an instance of a computer system in a layer abstracted from the actual hardware. Virtual machines share resources such as CPU, RAM and storage from the host or base machine. The base machines knows of these machines as regular files, but with the help of a virtualization platform also known as a hypervisor, these files can be converted to machines to run your applications. Virtual Machines can be stored as images and can be easily transported from one hardware to another. 


## Pros

  1. One of the major advantages of using virtual machines is the ability to run multiple operating systems on the same host or base machine. Thereby, it can help reduce the need to run multiple physical servers and has a huge impact on reducing costs and physical space requirements.
  2. Virtual Machines can be maintained, provisioned and transported easily. 
  3. If you are using virtual machines hosted on the cloud, you don't need to worry about the Physical hardware or OS updates, this would be taken care of by cloud providers.
  4. Virtual Machines provide isolation of resources from the host machine and also from other guest virtual machines sharing the same host, thereby providing a strong secure boundary between various applications.

## Cons

  1. Virtual Machines enact Physical servers and can become of large size due to added Application dependencies and have a large Operating System footprint.

  2. Virtual Machines contain operating systems installed on them and thereby might take a long time to startup. Especially, while applying the principles of continuous integration and delivery, if the virtual machine should be easily destroyable and deployabled when needed, the Operating System booting could introduce significant delays.



## The BC Gov Story

   BC Government has two datacenters, one located in Kamloops and the other in Calgary. The one is Calgary is mostly used to host Delivery and Test Environments and the one in Kamloops hosts the production environments.

### Application statistics

| Type of Software category | Application Archetype | Number of Apps on Virtual Machines |
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


### Applications Archetypes that can be hosted on Virtual Machines


### Best Practices to move from Physical Servers to Virtual Machines





                            