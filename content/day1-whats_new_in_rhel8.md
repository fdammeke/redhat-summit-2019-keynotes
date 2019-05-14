## What's new in RHEL 8?
--
## Subscriptions and release cycle
* Addons and offering stay the same
  * RHEL subscription
* Predictable release cycle per quarter year
  * Base os (10y support)
* More frequent application updates (like apache/nginx/..)
  * application streams
  * developer - build content at developers.redhat.com
--
## Tech stuff
* 4.18x kernel
* lvm6
* yum4 (frontend interface, backend based on dnf)
* systemd
* intel/ibm power/arm
--
## Performance improvements
* 10% cpu
* 30% storage
* 45% networking
--
## Upgrade
* Upgrades between RHEL 7 and 8 are done with leap
* LVM based filesystem snapshot backed by BOOM
  * Boot in initramdisk -> upgrade proceeds + selinux relabeling
--
## Deployment
* image-builder
  * iso - dvd installer
  * cloud image - ami / google format
* univeral base image (container)
  * ubi8-dev
  * rhel like container
--
## Changes
* Containers
  * docker = gone
  * new: podman
    * create a Dockerfile
    * build it with podman build
    * all root-less no privileges required
  * new: buildah / skopeo
--
## Changes
* System management
  * Red Hat insights - included in subscription
  * Intelligent information about operating system
  * tuned profiles
  * System roles
  * Crypto policies
    * affects a bunch of local applications
      * example: curl/wget/bind/ssh/..
--
## Changes
* Cockpit
  * webgui for the 'windows admin'
  * usual authentication method - password or ssh key
* Session recording
  * stored in journald
