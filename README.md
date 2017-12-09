# README #

This README shows how to build network for a company with VMware ESXi type-1 hypervisor using VyOS for routing.

### The network ###
![Topologija omre¾ja](docs/topology.png)  

### Setup

First you need to install VyOS. Then we can configure the interfaces. We can do this by running.
``` javascript
configure
set interfaces ethernet eth0 address '88.200.24.232/24'
set interfaces ethernet eth0 description 'ISP router'
set interfaces ethernet eth1 address 'fd00::1/64'
set interfaces ethernet eth1 description 'IPv6 only'
set interfaces ethernet eth2 address '192.168.2.1/24'
set interfaces ethernet eth2 description 'DMZ zone'
set interfaces ethernet eth3 address '10.2.0.1/24'
set interfaces ethernet eth2 description 'Employees'
commit
save
```
