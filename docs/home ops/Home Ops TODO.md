---
share: True
category: "Home OPS"
---
[[Project TODOS MOC]]

PROJECT: [[Home OPS]]

# TODOs

## Core
- [x] Setup [[Pre-Commit]]
- [x] Public Secretes using [[SOPS]]
- [x] Multi server setup [[Flux#Multicluster setup in one repo]]
- [x] Setup Clusters [[Flux#Bootstrap Examples]]
- [x] Setup cert-manger to manage certificates
- [x] Volumes and backups [[Longhorn]]
- [ ] Solution for automatic restore on initial setup.
- [x] Run both old and new Plex simultanously.
- [ ] Force update KS if changes are detected in dependency files.
- [x] Host Path for NFS mount.
- [ ] Rclone
	- [x] Dashboard
	- [ ] Logs

## Ansible
- [ ] Fix multipath [[Longhorn#Multipath mount issue]]
- [ ] Setup Flux keys [[SOPS#age-keys]]
- [ ] Setup  [[Flux]]
- [ ] Setup [[NFS]]


## Teraform
- [ ] Cloudflare
- [ ] Proxmox

## Media
- [x] Sonarr
	- [x] Apps
	- [x] Dashboard
	- [x] Logger
- [ ] Stash
	- [ ] App
	- [ ] Dashboard
	- [ ] Logger
- [ ] Radarr
	- [x] Apps
	- [ ] Dashboard
	- [ ] Logger
- [ ] Sabnzbd
	- [x] App
	- [ ] Dashboard
	- [ ] Logger
- [ ] Plex
	- [x] App
	- [ ] Logger
- [ ] Bazzar
	- [ ] App
	- [ ] Logger
- [ ] Ombi/Overseer
	- [ ] App
	- [ ] Logger

## APPS
#### Monitoring
- [x] Grafana
	- [ ] Persistent storage?
- [x] Loki
	- [ ] Persistent storage?