---
description: None
share: True
tag: None
---
Back [[Projects MOC]]


#### Context
Define what Home OPS is.

#### TODO: [[Home Ops TODO]]

#### Strategies
##### Branching
1. Make local **dev cluster** to deploy and map it to develop branch
2. Write specs to test changes
3. when all specs pass merge to master

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

#### Github Token COPY
```text
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
```


#### Flux
- Install: [[Flux#Installation]]
- Watch: [[Flux#Watch Kustomizations]]
- Bootstrap: [[Flux#Bootstrap Examples]]

#### Rancher
Install: [[Rancher#Install Rancher Without Traefik]]
Token: [[Rancher#See k8s token]]
Uninstall: [[Rancher#Uninstall]]


### ISSUES
#### K8s
Stuck in Termination: [[k8s#Patch Finalizer]]

#### Longhorn
Volume Stuck: [[Longhorn#Multipath mount issue]]

![File:Test image.jpg - Wikipedia](https://upload.wikimedia.org/wikipedia/en/9/95/Test_image.jpg)