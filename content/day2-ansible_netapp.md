## Ansible and NetApp
### Accelerating configuration and embracing infrastructure as code
--
## Official module support with official releases
* redhat certified and supported modules
  * docs.ansible.com - modules - storage - netapp
* 20+ element software modules
--
## Modules
* 60+ ontap software modules
  * 70% day-0 tasks
  * 95% day-1 tasks: hardening, onboarding vServer, new network interface
  * 98% day-2 tasks: create aggregates, volume, lun, mapping, igroup etc... - cover 2% by just executing netapp commands
  * soon: cluster create and cluster join
--
## Modules
* 60+ ontap software modules
  * software define ontap select
  * cloud based ontap
  * netapp modules communicate differently
    * communicate towards localhost and subsequently calls https
    * validate_certs: false
--
## Modules
* 60+ ontap software modules
  * netapp created roles not playbooks
    * na_ontap_vserver_create
      * create vserver
      * define protocols
      * create interface lifs
      * modify export policy
      * join AD
      * configure DNS
      * volumes / etc..
--
## Modules
* 60+ ontap software modules
    * na_ontap_snapmirror_create
      * automated setup is a +
      * some people say it's difficult
--
## Management
* the modules are idempotent !!
  * you can update settings on your cluster without breaking the previous ones set
* way faster than system manager
  * 96% increate in RTO
--
## Get started
* start with new volumes, new exports
* backport the most simple tasks first and work your way up to more difficult ones
--
## Issues
* vserver needs aggregates first
* disk add - one node/controller assigns all disks it can see
