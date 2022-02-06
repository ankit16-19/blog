---
share: True
category: "home-ops"
---
[[Home Ops]]


#### Install Rancher Without Traefik
```sh
export INSTALL_K3S_EXEC="server --no-deploy traefik"
curl -sfL https://get.k3s.io | sh -s -
```


#### See k8s token
```sh
cat /etc/rancher/k3s/k3s.yaml
```


#### Uninstall
```sh
/usr/local/bin/k3s-uninstall.sh
```