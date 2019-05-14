## Audit thy OpenShift
### Container runtime security with Falco
--
## OpenSource you say?
* Sysdig and Falco security are free opensource products
* Falco = sysdig secure (enterprise product)
* Sysdig performance analysis
* Lessons learned
  * pick your opensource project name wisely
  * don't brand your company with the same name as your opensource project
--
## Best practices
* Dockerfile
  * run as user
  * copy >> add
  * remove unnecessary packages and tools
    * (even tar/gzip/curl/telnet/nc/..)
* Images
  * tag images or use hash
--
## Best practices
* RBAC
  * users / service accounts
* K8S security policies
* secrets and certs
  * secure communication over the wire
  * rotate service account tokens
--
## Best practices
* Scan container images
  * anchore engine
  * Clair / Quai
  * vuls.io
  * openscap
--
## Best practices
* Falco runtime security
  * CNCF sandbox project
* Comparison with home security
  * intrusion prevention
    * password
    * 2FA
    * container image scanning
    * selinux
    * network policies
  * intrusion detection
    * kubernetes audit logging
    * falco anomaly detection
--
## Falco history
* history
  * tcpdump - ethereal - wireshard - sysdig - falco
  * snort : wireshark = sysdig : falco
* Falco how
  * old: kernel module (based on sysdig)
  * new: kernel >= 4.14 eBPF program
  * RPM installation
* Falco configure
  * rules
  * example: a rule that checks configmaps for credentials or credentials alter
--
## Alerting
* syslog / file / ..
* Reponse engine
    * kill pod / take other action
