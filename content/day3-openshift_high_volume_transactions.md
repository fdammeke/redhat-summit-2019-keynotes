## High volume secure transactions hosted on openshift (accenture)
--
* Accenture federal services
* What?
  * IOT devices - connected to AWS cloud + openshift
    * microcomponents
      * services
      * kafka
      * glusterfs
      * database backend
--
* lessons
  * strict s2i build process
    * control and consistency
    * devs can't do anything
    * openshift catalog, request at tech-team
  * flyway sql versioning
  * namespace per service
  * routing / dns wildcard
  * access control
--
* more lessons
  * quotas are important
  * bad quota estimation from dev teams -> metrics plugin
* akka - reactive manifesto
  * built on scala
  * based on the actor model
