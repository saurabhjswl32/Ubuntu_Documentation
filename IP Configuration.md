## IP Configuration

Go to etc/netplan
```
cd /etc/netplan

```

edit yaml file
```
vim file_name

```

Enter following details
```
# Let NeworkManager manage all devices on this system
network:
  version: 2
  renderer: networkd
  ethernets:
      enp12s0:
          dhcp: no
          addresses: [172.27.21.#]
          gateway: 172.27.16.254
           nameserver:
               addresses: [172.27.16.#]

```
```
netplan apply
```
