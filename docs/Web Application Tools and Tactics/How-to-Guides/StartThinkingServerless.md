---
layout: default
title: Start Thinking Serverless
parent: How-to-Guides
nav_order: 2
---

## How to go serverless

  You can adopt any of the given three strategies when you are thinking of migrating to a serverless architecture.

  1. **Leapfrog**: While using this strategy, you skip any iterim steps and directly migrate your applications from legacy infrastructure to serverless cloud.

  *Considerations*: There will be significant application rewrites involved in this process. You will need to make your application event-driven and experiment how it would work with serverless eventdriven functions. Your applications are recommended to be asynchronous and should adhere with the cloud native 12 factors. This strategy is recommended for developers with expertise in using serverless functions. 

  2. **Organic**: With this approach you gradually lift and shift your application to Cloud. You can keep your existing applications intact by moving them to virtual machines or with possible minimal rewrites to containers. While adopting this strategy, the developers would have the liberty to experiment low risk scenarios such a batch jobs, cron jobs or log processing using serverless functions and then move towards experimenting parallel jobs and data transformations using event-driven solutions. 

  *Considerations*: While adopting this strategy, you can introspect on how serverless and microservice architecture will help transform your business by inducing agility, innovation and reducing total cost of ownership. By lifting and shifting one application and moving a low risk production workload to serverless cloud, you can pave way to automate this process and apply the lessons learned to further applications.

  3. **Strangler**: Using this approach, you would decompose all your monolithic applications incrementally by creating APIs and building event-driven components that gradually replace components of the legacy application. You can build API endpoints to point to old and new components to maintain a safe balance and ensure you are full ready and risk free before you can fully adopt serverless solutions.

  *Considerations*: While adopting this strategy, you need to analyse the application and it components and then decouple the applications into microservices. Along with microservices, strangle your data, define the data distribution and design how data will be stored. Then, you will need to decide how each application and data store component will scale independently based on demand. Schedule based tasks/cron jobs are excellent candidates for implementation using serverless functions. During this process, you can also decide how to refactor and enhance your application functionality without affecting the current implementation. This is most commonly adopted pattern while moving to serverless architecture.

  ## Cost Considerations

  While migrating your applications to serverless, it is important to consider the following:

  1. Compare the infrastructure cost to run your workload on serverless compute as well as running it on containers or server based systems.
  2. Estimate the costs for development efforts i.e., to plan, architect and provision resources.
  3. Costs to maintain the application on server based systems, containers and on serverless cloud.

