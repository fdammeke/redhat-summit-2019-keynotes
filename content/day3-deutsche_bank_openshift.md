## Hybrid cloud infrastructure
### How Deutsche bank uses openshift on all clouds
--
## Timeline
* 43% banking apps on openshift
* 2019 hybrid cloud
* cloud first for new deployments
* 27 clusters - multi-tenant environments
--
## Multi-region
* 3 infra vendors
  * running openshift on top of the vendor - abstraction layer
* terraform / ansible deployments
* moved to tower to manage / run ansible playbooks,
  * it became impossible to manage 900 nodes
* running multiple clusters is hard
  * config drift is deadly
  * stability vs new client features and capabilities can become a trade off
--
## Goals
* platform and client goals didn't align everywhere
* multi-tenant means client requirements become key
* avoid snow-flaking
* portability of workloads is important
* the platform has to be defensive
  * operation procedures
--
## Delivery
* People are builders and consumers
  * platform as a product
  * one team member that acts as a proxy
--
## Why openshift over native k8s?
  * as a bank required enterprise support
  * the engineering effort and way of working difference
  * why not managed kubernetes?
    * abstraction layer
    * each cloud vendor has it's own implementation
    * while running openshift on the cloud provider, the service becomes identical
  * they don't consume any cloud provider specific services
    * prevent snowflakes by consuming dbaas on aws compared to google
    * ensure max portability
--
## The process of getting up and running
* Automate everything or die
* Continuous improvement
* Iterative releases
* Scrum of scrums
* Not allowed to pull from docker hub
  * clients and vendors expect to be able
* Prevent having 10 ways to deploy for example mongodb on the clusters
