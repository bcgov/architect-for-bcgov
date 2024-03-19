---
title: High Availability is not Disaster Recovery
permalink: resilience-design-principles.html
---

# High Availability is not Disaster Recovery

Every application is different and needs to be architected differently to optimize performance, efficiency, reliability and costs. However, there are some generic design principles that can be applied to establish a well architected system. 

## Terminology 

<b> Reliability </b>: If the components in a cloud computing system perform their functions and fail rarely, the system is said to be reliable. 


<b> Availability </b>: Availability is the measure of percentage of a time period during which the system is able to respond to user requests. For example, A cloud computing system is said to be 99. 9% if its scheduled or unscheduled downtime totals 3.65 days in a year or  14.4 minutes in a day 

<b> Redundancy </b>: Redundancy refers to the duplication of certain components or functions within a system with the intention to increase its reliability and availability

<b> Resilience </b>: Resilience is the ability of a system to recover on its own (self-heal) after a system failure.

<b> Fault Tolerance </b>: Fault tolerance is the ability of a system to continue functioning during the event of a failure to one or more of its components.

<b> Durability </b>: Durability of a system is its ability to meet user needs for a long period of time.

<b> Disaster Recovery </b> : Disaster Recovery is an organization's ability to restore access and functionality to IT infrastruture after a disaster event ,whether natural or caused by human action.

<b> Recovery Point Objective </b>: Recovery Point Objective (RPO) is the definition of acceptable amount of data loss measured in time for a given system. It is said that after a system downtime, the system can recover from the failure within the time defined as "RPO" for the system.

<b> Recovery Time Objective </b>: Recovery Time Objective (RTO) is the time it takes a system after a downtime/disruption to restore the service. For eg, a system can be maximum unavailable for the time defined as its "RTO".


### Metrics for measurement

<b> Parameter </b> | <b> Metrics </b> | <b> How is it calculated </b> | <b> Ideal Value </b> |
------------------ | --------------- | ----------------------------- | -------------------- |
Reliability        | Mean Time To Failure(MTTF), Mean Time To Recover(MTTR) and Mean Time Between Failures (MTBF)  | MTTF is the average of the time between 2 consecutive failures, MTTR is the average of the time to recover and MTBF = MTTF+MTTR |  All the three metrics should be low to signify high reliability |
Availability       | Uptime, Downtime, Agreed Service Time  | Availability = ((Agreed Service Time) - Downtime)/ Agreed Service Time | *Availabilty chart is given below |
Resilience         | Mean time to repair (MTTR) | MTTR is the average of the time to repair a system post failure | Lower the MTTR, higher the resilience
Fault Tolerance    | RPO, RTO | a fully fault tolerant system generally has zero downtime | RPO = RTO = zero


#### System Availability Chart

<b> Availability Level measure in uptime </b> | <b> Allowed downtime per year </b> | <b> Allowed downtime per quarter </b> | <b> Allowed downtime per day </b> |
--------------------------------------------- | ---------------------------------- | ------------------------------------- | -------------------------------- |
90% | 36.5 days | 9 days | 2.4 hours |
95% | 18.25 days | 4.5 days | 1.2 hours | 
99% | 3.65 days| 21.6 hours | 14.4 minutes |
99.5% | 1.83 days | 10.8 hours | 7.20 minutes |
99.9% | 8.76 hours | 2.16 hours	| 1.44 minutes |
99.95% | 4.38 hours | 1.08 hours | 43.2 seconds |
99.99% | 52.6 minutes | 12.96 minutes | 8.64 seconds |
99.999% | 5.26 minutes | 1.30 minutes | 0.87 seconds |	

## Design Principles

To aim for higher availability, resilience, durability, reliability and fault tolerance of your systems and achieve close to zero RTO and RPO, it is recommended to incorporate some design principles while designing your application/system.

 ### 1: Enable scalability
 1.1 Scale horizontally to increase aggregate workload availabilty
 1.2 Stop guessing capacity and scale vertically to add resources to your system to prevent under- or over- utilization of resources

### 2: Automate your environment
 2.1 Automatically recover from failures
 2.2 Manage change through automation 
 2.3 Automate with architectural experimentation in mind
 2.4 Perform operations as code
 2.5 Automate security best practices

### 3. Use disposable resources
3.1 Make frequent, small. reversible changes

### 4. Loosely couple your components

### 5. Design services, not server
5.1 Use managed services

### 6. Choose the right compute, storage, network, database solutions
6.1 Consider mechanical sympathy

### 7. Avoid single points of failure

### 8. Optimize for cost benefits
8.1 Analyze and attribute expenditure
8.2 Measure overall efficiency

### 9. Use caching

### 10. Secure your system at every layer
10.1 Implement a strong identity foundation
10.2 Maintain traceability
10.3 Protect data in transit and at rest
10.4 Keep people away from data
10.5 Prepare for security events

### 11. Test systems at production scale

### 12. Consider evolutionary architecture

### 13. Drive architectures using data

### 14. Improve your architecture continuously and experiment more often
14.1 Automate simulations of system failure and apply recovery processes to test the same.
14.2 Refine operation procedures frequently
14.3 Anticipate failure and learn from all operation failures
14.4 Implement observability for actionable insights
14.5 Democratize advanced technologies





     