---
share: True
category: "Home OPS"
---
Back [[Projects MOC]]


#### Context
WIP. Define what Home OPS is.

#### TODO: [[Home Ops TODO]]

#### Dependencies
- [[Rancher]] :  To create and mange k8s clusters
- [[Flux]] : To manage [[GitOps]]
- [[Longhorn]]: To manage volume and backups
- [[NAS]] : To store all the data and backups.

#### Server Setup
##### Github token: [[Github#Github token]]
- Prod server: [[Flux#Prod server Home OPS]]
- Dev server: [[Flux#Dev Server Home OPS]]
- Save age keys: [[SOPS#age-keys]]
- Setup sops: [[SOPS#Installing keys in flux]]

#### Flux
- Install: [[Flux#Installation]]
- Watch: [[Flux#Watch Kustomizations]]
- Bootstrap: [[Flux#Bootstrap Examples]]

#### Rancher
Install: [[Rancher#Install Rancher Without Traefik]]
Token: [[Rancher#See k8s token]]
Uninstall: [[Rancher#Uninstall]]


## ISSUES

#### K8s
Stuck in Termination: [[k8s#Patch Finalizer]]

#### Longhorn
Volume Stuck: [[Longhorn#Multipath mount issue]]