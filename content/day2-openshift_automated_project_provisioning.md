## Automated project provisioning
### using the operator software developer kit
--
## Usecase
* SIX: IT provider for swiss banks
* Used operator the resolve the integration with internal services
--
## Promote your platform
* Explained the  benefits of the OpenShift project to company
  * project marketing
    * external at redhat summit
    * internally: OpenShift expo - invite employees to join event to explore openshift
      * awareness!!
      * inspiration and transition movie - lol
--
## Infrastructure
* virtual machine based
* 3 on premise clusters
* 2 datacenters - low latency
* 30+ network zones - dedicated routers that provide network traffic in zones
--
## Project onboarding
* Resource quota and ranges - but specific to project
* Chargeback
* Prometheus monitoring
* Logs sent to splunk with special token
--
## Project provisioning before
* Before: templates to deploy projects
  * difference between template files in git and real-life state of project
--
## Project provisioning after
* After: operator SDK
  * kubernetes manages kubernetes: project lifecycle control
  * project provisioning automation
  * developers can create projects (self-written frontend)
    * user -> IaaS portal - > OpenShift -> project provisioning
    * portal calls OpenShift api using RBAC service account
    * portal form based on VRO workflow
      * name + displayname
      * resource limits
      * service code (workorder)
--
## Operator benefits
* Follow the operator upstream release cycle of operator sdk
* Easy to apply changes
* Recurring changes ported to operator
