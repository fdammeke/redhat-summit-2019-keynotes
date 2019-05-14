## Ansible and Cisco
### Multi cloud automation with ansible and ACI
--
## Support
* fully supported by ansible (2.7/2.8)
  * the ACI modules are part of ansible core
  * use them to: access policies, tenants, filter, contract, vrf, epg, ...
* what
  * use ansible to provision infrastructure
  * if you want to do stuff at scale, don't use the UI (cisco advise)
--
## ACI Releases
* ACI multi-pod 2.0 - layer 2 streched
* ACI multisite 3.0 - disconnect control plane, single place to define your rulebase
* ACI remote leaf 3.1
* Virtual ACI 4.0
* Cloud ACI 4.1 - extend data and controlplane into multi datacenter
  * amazon security group
  * different security concepts in different cloud providers
  * one pane of glass - exact same security requirements are transparently implemented
--
## Ansible ACI + MSO modules
* ACI + MSO modules
  * new in ansible 2.8 - MSO (multi site orchestrator)
* how to use the ACI modules
  * you can easily document and version how your infrastructure looks (YAML)
  * there are a lot of modules (60+) but that's intentional
    * your configuration can be very modular
    * everyting for day-2 operation is possible
    * aci_rest module to do anything that's not defined in a module
--
## Ansible ACI + MSO modules
* ACI + MSO modules
  * one APIC connection, delegate_to: localhost
  * build an application
    * tenant - vrf - 3 BD - EPG + contracts
    * what would you normally do
      * create it all manually - filter - contract - subject - filter binding - epg binding
--
## Ansible ACI + MSO modules
* ACI + MSO modules
  * how would you do it automated? Same steps as GUI but fully automated
    * create a yaml configuration (yaml anker in vars)
    * yaml: tenant
    * yaml: vrf
    * yaml: bd (bridge domain)
    * yaml: bd subnet
    * yaml: ap (application profile)
    * yaml: epg
--
## Why?
* It's damn fast!
* It's idempotent!
  * only changes are made to stuff you define
  * only changes are made if changes are required, otherwise it will return OK.
--
## Tips
* optimize your ACI login!!
  * 10/15 logins per minute (dDoS protection)
  * certificate/signature based authentication is recommended to bypass this problem
  * certificate import can even be realised with an ansible playbook -> first task = import cert
--
## Modules vs roles
* aci_module role
* easy kick-starter
* define one role and it will automatically implement the 60+ modules
* the role is an example how to fully automate your setup
* TAC automate 25x
* hiera like YAML with configuration depth
* module contribution is allowed and highly appreciated
--
## Presentation
[https://docs.ansible.com/ansible/latest/scenario_guides/guide_aci.html](https://docs.ansible.com/ansible/latest/scenario_guides/guide_aci.html)

Presenter: Ramses Smeyers
rsmeyers@cisco.com if you want the original slides
