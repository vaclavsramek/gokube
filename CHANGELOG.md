# GoKube Release Notes

## Version 1.36.0 - 07/08/2025
* Bump to minikube v1.36.0, K8S v1.33.1, helm v3.18.3, docker 28.3.1
* Change to get docker from download.docker.com
* ChartMuseum retries incremented and new function to check readiness.
* Change to get helm-image from ThalesGroup https://github.com/ThalesGroup/helm-image
* Change to get kubectl from dl.k8s.io

## Version 1.35.0 - 02/05/2025
* Bump to minikube v1.35.0, K8S v1.32.0, helm v3.17.0, and stern v1.32.0

## Version 1.34.0 - 11/27/2024
* Bump to minikube v1.34.0, K8S v1.31.0, helm v3.16.3, and stern v1.31.0 
* Added K9s v0.32.7 to manage and interact with Kubernetes clusters.

## Version 1.33.0 - 06/03/2024
* Bump to minikube v1.33.1, K8S v1.30.0, helm v3.15.1
* Fixed issue when adding swap memory and disk already exists, skip the creation.

## Version 1.32.0 - 04/05/2024
* Bump to minikube v1.32.0, K8S v1.28.3, helm v3.14.3
* Added swap memory option MINIKUBE_SWAP. Disabled by default (0).

## Version 1.31.0 - 10/07/2023
* Bump to minikube v1.31.2, K8S v1.27.4, helm v3.12.3

## Version 1.29.2 - 03/09/2023
* Bump to helm v3.11.2
* Fixed snapshot that were always removed after reset

## Version 1.29.1 - 03/08/2023
* Added --force to avoid SSH check issues when starting VM

## Version 1.29.0 - 03/07/2023
* Bump to minikube v1.29.0, K8S v1.24.10, helm v3.11.1
* Added configuration for container runtime (to prepare switch to containerd)

Note: containerd is currently not working for insecure registry set as CIDR and behind HTTP proxy (see https://github.com/kubernetes/minikube/issues/15596 and https://github.com/kubernetes/minikube/issues/15597)

## Version 1.28.2 - 02/27/2023
* Fix to create snapshots when no snapshots exist [#28](https://github.com/gemalto/gokube/pull/28)

## Version 1.28.1 - 01/17/2023
* Fixed save command when snapshot did not exist previously [#26](https://github.com/gemalto/gokube/pull/26)

## Version 1.28.0 - 11/16/2022
* Bump to minikube v1.28.0, K8S v1.24.8, helm v3.10.2

Please note v1.27.1 is not mounting Windows user directory inside minikube VM (because of a minikube [issue](https://github.com/kubernetes/minikube/issues/14465))

## Version 1.27.1 - 10/17/2022
**NOTE: Starting from this version, gokube is only compatible with helm 3.7+ (major change is chart push plugin command name is now 'cm-push' to not clash with new helm 3.7+ OCI 'push' command)**

* Bump to minikube v1.27.1, K8S v1.22.15, helm v3.10.1, stern 1.22.0

## Version 1.25.5 - 06/22/2022
* Bump to K8S v1.22.11

## Version 1.25.4 - 04/14/2022
* Added --dns-domain flag to choose cluster DNS domain

## Version 1.25.3 - 04/04/2022
* Bump to helm-image v1.0.7, docker 20.10.14

## Version 1.25.2 - 03/31/2022
* Bump to minikube v1.25.2

## Version 1.25.1 - 02/16/2022
* Bump to minikube v1.25.1, K8S v1.20.15

Please note latest minikube versions integrates new host-only networking constraints from VirtualBox, which means it *may* be mandatory to upgrade VirtualBox (to at least 6.1.28)

Please note helm 3.6 branch is kept by default for now because of incompatibility between helm-push plugin and newly introduced OCI push command in helm 3.7+

## Version 1.22.1 - 08/24/2021
* Bump to K8S v1.20.10, helm-image v1.0.6, helm-spray v4.0.10
* Added --keep-vm flag for init command  
* Multi snapshot management (finalized)

## Version 1.22.0 - 08/10/2021
* Bump to minikube v1.22.0, K8S v1.20.9, helm v3.6.3, helm-image v1.0.5, helm-spray v4.0.9
* Increased timeout for chartmuseum availability  
* Smarter implicit upgrade
* Multi snapshot management (draft)

## Version 1.17.1 - 02/04/2021
* Bump to helm-spray v4.0.7
* Implicit upgrade will be applied again if last VM creation did not fully succeed (to ensure helm plugins will always be installed) 

## Version 1.17.0 - 02/02/2021
* Bump to minikube v1.17.1, helm v3.5.1, helm-image v1.0.4

## Version 1.16.1 - 01/25/2021
* Bump to K8S v1.18.15
* Revert to docker 19.03.14 (because of issue with docker login on Win7)
* Did not bump yet to minikube v1.17.0 (because it now requires <host>:<port> for insecure registries)
* Added commands to manage snapshots

## Version 1.16.0 - 01/04/2021
* Bump to minikube v1.16.0, K8S v1.18.14, docker 20.10.1

## Version 1.15.1 - 11/19/2020
* Bump to minikube v1.15.1
* Changed chartmuseum chart repo following helm stable repo deprecation

## Version 1.15.0 - 11/16/2020
* Bump to minikube v1.15.0

## Version 1.14.2 - 11/13/2020
* Bump to minikube v1.14.2, K8S v1.18.12, helm v3.4.1, helm-push v0.9.0

## Version 1.14.1 - 10/26/2020
* Bump to minikube v1.14.1, K8S v1.18.10, helm v3.4.0, helm-spray v4.0.5

## Version 1.14.0 - 10/14/2020
* Bump to minikube v1.14.0, helm v3.3.4, helm-spray v4.0.3

## Version 1.13.1 - 09/21/2020
* Bump to minikube v1.13.1, helm v3.3.3, helm-spray v4.0.2

## Version 1.13.0 - 09/17/2020
* Bump to minikube v1.13.0, K8S v1.18.9, helm v3.3.1, helm-image v1.0.2

## Version 1.12.3 - 08/13/2020
* Bump to minikube v1.12.3

## Version 1.12.2 - 08/12/2020
* Bump to minikube v1.12.2, K8S v1.18.6, helm v3.3.0

## Version 1.12.1 - 07/23/2020
* Bump to minikube v1.12.1

## Version 1.12.0 - 07/10/2020
* Bump to minikube v1.12.0, K8S v1.18.5, docker 19.03.12, helm-image v1.0.1

## Version 1.11.0 - 06/20/2020
* Bump to minikube v1.11.0, K8S v1.18.3, helm v3.2.4, helm-spray v4.0.1
* Added new helm image plugin v1.0.0

## Version 1.10.0 - 05/12/2020
**NOTE: Starting from this version, gokube is only compatible with helm 3**

* Bump to minikube v1.10.1 (1.10 is buggy)
* Bump to helm-spray v4.0.0

## Version 1.9.2 - 04/04/2020
* Bump to minikube v1.9.1
* Reduced the timeout to check for new version of gokube

## Version 1.9.1 - 03/31/2020
* Shows a warning if not using the latest gokube release

## Version 1.9.0 - 03/27/2020
* Bump to minikube v1.9.0, K8S v1.18, docker v19.03.8
* Upgrade is now also possible upon restart (when we don't want VM to be respawn)

## Version 1.8.2 - 03/14/2020
* Upgrade is automatically done the first time you execute a new version of gokube
* Miniapps URL repo fixed to match new thalesgroup organization
* Bump to kubernetes v1.17.3, helm 2.16.3, minikube v1.8.2

## Version 1.8.1 - 02/08/2020
* Bump to kubernetes v1.17.2, minikube v1.7.2

## Version 1.8.0 - 12/19/2019
**THE BIG ONE**

* Bump to kubernetes v1.16.4, minikube v1.6.1, helm v2.16.1 and docker 19.03.3
* Support of Virtualbox 6 (with the limitation that no other VMs shall be running during gokube init)
* Added warning messages on gokube stop to prevent crashes/unstabilities on VM restart
* Support of environment variables to download more recent versions of dependencies (to avoid generating a new version of gokube each time)
* Added pause and resume commands

Supported environment variables are:
- KUBERNETES_VERSION (ex: "v1.16.4")
- MINIKUBE_VERSION (ex: "v1.6.1")
- DOCKER_VERSION (ex: "19.03.3")
- HELM_VERSION (ex: "v2.16.1")
- HELM_SPRAY_VERSION (ex: "v3.4.5")

As recent minikube versions automatically selects the best hypervisor, please note no tests have been made yet for Win10/Hyper-V contexts

## Version 1.7.7 - 10/16/2019
* Update helm-spray to 3.4.5 [#42](https://github.com/gemalto/helm-spray/pull/42)

## Version 1.7.6 - 09/23/2019
* Fix for 1.7.5 "Unable to read config file" [#13](https://github.com/gemalto/gokube/issues/13)

## Version 1.7.5 - 09/18/2019
* Enhance management of default kubernetes version (hotfix)

## Version 1.7.4 - 09/12/2019
* Enhance management of default kubernetes version
<p>Changing the kubernetes version with the environment variable did not prevent a potential upgrade of kubernetes
upon a VM restart (e.g. gokube stop / gokube start). The desired version of kubernetes is now stored under
.gokube/config.yaml and is used for init and start commands</p>

## Version 1.7.3 - 09/11/2019
* Enhance management of default kubernetes version
<p>You can change the default kubernetes version (v1.10.13) for your VM in setting a KUBERNETES_VERSION global environment variable</p>

## Version 1.7.2 - 09/10/2019
* Bump to helm spray v3.4.4 (which fixes issues on liveness/readiness for id-provider) [#12](https://github.com/gemalto/gokube/pull/12)

## Version 1.7.1 - 08/14/2019
* Bump to minikube v1.3.1 (which fixes a TTY/PTY issue preventing gokube init progress bar to be displayed)

## Version 1.7.0 - 08/06/2019
* Bump to minikube v1.3.0 (to benefit from the NAT DNS options), bump to helm spray v3.4.3 [#10](https://github.com/gemalto/gokube/pull/10)

## Version 1.6.2 - 05/29/2019
* kubernetes-dashboard not always patched [#9](https://github.com/gemalto/gokube/pull/9)

## Version 1.6.1 - 05/22/2019
* Fix for kubernetes-dashboard not always patched [#8](https://github.com/gemalto/gokube/issues/8)

## Version 1.6.0 - 04/02/2019
* Bump to minikube v1.0.0 [#7](https://github.com/gemalto/gokube/pull/7)

## Version 1.5.0 - 02/08/2019
* Bump to helm-spray v3.2.0 and stern v1.10.0 [#6](https://github.com/gemalto/gokube/pull/6)

## Version 1.4.0 - 11/21/2018
* Bump to monocular v1.2.0 (that support http proxy)
* Bump to docker v18.06
* Bump to k8s v1.10.9
* Add docker image 'mongodb' in cache for monocular
* Add support of any-proxy (for transparent proxy)
* Add support of --cache-images
* Patch kubernetes-dashboard service to expose it on nodePort: 30000

## Version 1.3.0 - 10/15/2018
* Add option for using a specific version for Minikube
* Add option for using a specific version for Helm
* Add option for using a specific fork for Minikube

## Version 1.2.0 - 10/09/2018
* Updated Minikube to 0.30.0
* Updated Kubectl to 1.12.0
* Remove directories: '.kube' and '.docker' before upgrading gokube
