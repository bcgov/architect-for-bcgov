---
title: Application Design Principles for OpenShift
sidebar: ea_sidebar.yml
permalink: app-design-principles-openshift.html
---

## Design Principles
 
### 1: Build Once, Deploy Multiple Times

Build your application image in the Tools Namespace and deploy the image in the Dev, Test and Prod namespaces. In order to do this using a CI/CD workflow, it is important to build and deploy using build and deployment templates. Creating deployments using the console would deter redeploying if the pod comes down for maintenance. After the openshift build process, the image is stored in the imagestreams object with the Tools Namespace. There are two known methods to deploy images to the Dev,Test, Prod Namespace after the build process:
1. Tag the image in the dev, test, prod namespaces within your CI/CD workflow once the build process is complete using the command:

```
oc tag <license-plate>-tools/image-name  <license-plate>-<dev/test/prod>/image-name
```

This commands needs to be run each time the image is built.

To perform this process, it is essential to provide permissions to the service account, image-puller in dev/test/prod namespace to be access the imagestreams in tools namespaces. This can be done using the command:

```
    oc policy add-role-to-user \
    system:image-puller system:serviceaccount:<license-plate>-tools:default \
    --namespace=<license-plate>-<dev/test/prod>
```

This command only needs to be run once.

2. Deploy the Image from the tools namespace, but make sure that when you use this method, that you do not delete the image so that if and when the pod requires to come back up, it does not throw an error due to unavailability of the image.

To perform this process, it is essential to provide permissions to the service account, image-puller in dev/test/prod namespace to be access the imagestreams in tools namespaces. This can be done using the command:

```
    oc policy add-role-to-user \
    system:image-puller system:serviceaccount:<license-plate>-tools:default \
    --namespace=<license-plate>-<dev/test/prod>
```

This command only needs to be run once.

To understand more about images and image tags, Click [here](https://mvp.developer.gov.bc.ca/docs/default/component/platform-developer-docs/docs/build-deploy-and-maintain-apps/imagestreams/).

### 2. Zero Trust Network 

By design all pods in OpenShift are accessible to other pods within the cluster as well as to external endpoints through a route. To prevent data breaches, the concept of zero trust network works on the principles of never trust, always verify. From OpenShift version 4.10, CLAB, KLAB, SILVER, GOLD, GOLD-DR clusters are now supporting limited Egress network policies. KLAB2 and Emerald clusters use a different SDN technology (VMWare NSX-T) which also support and require Egress Network Policies. The platform-services-controlled-default network policy controlled by the platform administrators is applied to all namespaces on OpenShift and will be applied even if you delete it. This policy enforces zero trust network and denies all access by default. As a responsible developer, you need to ensure you do not open all access to your pods and build network policies that only allow necessary access.

To learn how to apply network policies, click [here](https://mvp.developer.gov.bc.ca/docs/default/component/platform-developer-docs/docs/platform-architecture-reference/openshift-network-policies/).

### 3. Always run at least 2 pods

Openshift pods are meant to be transient or ephemeral. To ensure high availability, it is therefore important to atleast run 2 pods and design your application to be able to operate on more than one instance. Running multiple pods can be done by setting the following field within the deployment config in your deployment template.

```
 spec:
   replicas: <number of replicas (more than 2)>
```

### 4. Spread your pods across nodes

It is not desirable to have all the pods or replicas on the same node within the OpenShift cluster, which leaves a risk of downtime of your application when the node is taken down for maintenance. OpenShift already does a good job of spreading out the pods across nodes based on resource availability and the general recommendation is not to interfer with OpenShift's scheduling policy. However, if you do require to enforce the behavior, a pod anti-affinity rule can be set up to prevent OpenShift from scheduling pods of a particular service on the same node. To read more about setting an anti-affinity rule in your deployment configuration, click [here](https://mvp.developer.gov.bc.ca/docs/default/component/platform-developer-docs/docs/automation-and-resiliency/app-resiliency-guidelines/#examples)

### 5. Define a pod disruption budget

Even with the anti-affinity rule in place and the OpenShift's pod scheduling policy, there is a chance that multiple pods could land on the same node or there might be an instance when the platform administrator decides to take down multiple nodes down for maintenance at the same time. To prevent your pods from going down all at once, you can set up a pod disruption budget. A pod disruption budget defines the minimum number of pods that must be available simultaneously. To read more about setting pod disruption budgets, click [here](https://mvp.developer.gov.bc.ca/docs/default/component/platform-developer-docs/docs/build-deploy-and-maintain-apps/maintain-an-application/#pdbs-pod-disruption-budgets)

### 6.  Do not use local/host path storage

Using local or hostPath storage will tie pods to the nodes where the storage exists, making it impossible for the pods to migrate during a maintainence activity.

### 7. Design your application so that it can tolerate pods going down

Your application pods will be killed during a node maintenance activity. OpenShift initially sends a SIGTERM to the pod which allows time for the app to shutdown. If the app doesn't shutdown within a given timeframe, OpenShift would then send a SIGKILL to the application process which would kill the process instantly without leaving time for existing client sessions to end. The application therefore needs to be designed so that it can quickly clean up when it recieves a SIGTERM and the server-side application needs to be stateless so that request for inflight client sessions can resume without hassles on a different pod. If the server-side application needs to maintain state, it has to be persisted using a cache or a database so that it can be retrieved by other pods.

### 8. Use resources graciously

The OpenShift platform is currently free for ministry teams to deploy their applications. However, this is not the case in Public Cloud and there is also a possibility that the OpenShift platform will be charged in the future. The application will be charged based on CPU, Memory and Storage resource usage and therefore it is essential to consistently monitor your application and ensure the CPU and memory requests and limits are adjusted according to usage. It is also essential to ensure that you are caching and managing storage wisely. It also becomes important to monitor the network traffic to ensure that you are not spending money on network resources unwisely. To read more about how to manage CPU and memory resources, click [here](https://mvp.developer.gov.bc.ca/docs/default/component/platform-developer-docs/docs/automation-and-resiliency/application-resource-tuning/).





