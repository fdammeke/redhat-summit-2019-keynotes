## Building production ready container images
--
### Problem
* Building container images is fun
* But without documenting the content and built strategy it will become a pain to upgrade in 2-3 years
* Bontainer images are in tar format
  * it causes a lot of pain to size your registry correctly
--
### Standerdize your base images
* RHEL base image (ubi)
* Dicipline will ease image sizing
--
### Minimize
* Limit the content in the image that serves the workload
### Delegate image builds
* core container build -> middleware container build -> application code
* base images on each other and empower others to depend on your images
### OpenShift online build system
* All container images hosted on registry.access.redhat.com are built using the openshift-buildsystem
