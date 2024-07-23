
## Static IP Setting

Step 1: Goto Direcrtory 
```
cd /etc/netplan

```

Step 2: Now edit file if file
```
01-network-manager-all.yaml.

```
Step 3: Enter these enteries
```
# Let NetworkManager manage all devices on this system
network:
  version:2
  renderer: networkd
  ethernets:
      enp12s0:
          dhcp: no
          addresses: [172.27.#.#/16]
          gateway4: 172.27.16.#
          nameservers:
              addresses: [172.27.16.#]
```