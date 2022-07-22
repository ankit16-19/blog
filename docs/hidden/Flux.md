---
share: True
category: None
---
[Github](https://github.com/fluxcd/flux)
#### Watch [[Kustomization]]
```sh
flux get kustomizations --watch
```


#### Installation
```sh
brew install flux
```


### Bootstrap Examples

#### Prod server Home OPS
```sh
flux bootstrap github \
  --context=default \
  --owner=ankit16-19 \
  --repository=home-ops \
  --branch=main \
  --path=./flux/clusters/prod \
  --personal
```


#### Dev Server  Home OPS
```sh
flux bootstrap github \
  --context=test \
  --owner=ankit16-19 \
  --repository=home-ops \
  --branch=test \
  --path=./flux/clusters/dev \
  --personal
```


### Multicluster setup in one repo
Deploying multiple cluster using single repositories, Use cases could be: Deployed on different env with different params, token, api keys, resources.

#### Branching Strategy
Keeping multiple branches to track changes, i.e keeping all cluster under cluster folder.
i.e [Home OPS repo structure](https://github.com/ankit16-19/home-ops/tree/main/flux)
```sh
--repo-root
---clusters
----prod
----dev
```

Here we have two cluster bootstrapped using Flux. [[Flux#Bootstrap Examples]].
These servers can keep [[Kustomization]] to include other source folder ie. apps, core, crds.

##### To override params based on different env
- We can use different root folders but this will lead to lot of duplicated code, Alternatively we can make use of [[Flux#Post Build]] feature. [Home Ops repo Example](https://github.com/ankit16-19/home-ops/blob/main/flux/clusters/prod/apps.yaml#L20) 
- Following above keeping track of similar config in different env will also result in lot of code duplication, We can take advantage of the fact that [[Flux#Post Build]] applies config based on the latest value, so if we keep all them in incremental order ie. base-config first and env config later. This will save us from repeated configs.



### Overriding expired Deploy token.
adding  `--token-auth=true` to bootstrap command will override the Deploy tokens.