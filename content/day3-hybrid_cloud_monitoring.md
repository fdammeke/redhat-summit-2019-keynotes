## Hybrid cloud monitoring
### OpenShift on AWS
--
* Helvetia - swiss insurance company
* AWS + OpenShift
  * AWS direct connect to backend
  * S3/EFS/EBS/RDS
* AWS + dynatrace
--
* monitoring stack
  * amazon based -> cloudwatch
  * openshift based -> prometheus
    * thanos for long term metrics storage
      *
    * alerting - slack integration
    * implementation
      * kube-state-metrics
      * node-exporter
      * blackbox-exporter (https/dns/tcp checks)
  * application based -> dynatrace
    * APM for springboot etc
