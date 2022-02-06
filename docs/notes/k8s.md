---
share: True
---
#### Patch Finalizer
if something is stuck in Termination state forever, you can remove the finalizers to help in RIP.
```sh
kubectl patch --type-- --name-- -p '{"metadata":{"finalizers":null}}' --type=merge
```