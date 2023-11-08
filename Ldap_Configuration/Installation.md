# Ldap Configuration in Ubuntu

## Install Ldap
```
apt -y install libnss-ldap libpam-ldap ldap-utils nscd autofs 
```

## Configuratin Setting
```
URI:- ldap://ldap.cse.iitk.ac.in

BASE:- ou=cse,o=iitk,dc=ac,dc=in

ldap version choose "3"

local root Database admin choose "no"

LDAP database require login choose "no"
```

## Copy auto.users, auto.master & fullchain.pem
```
scp cse@host_name:/home/cse/auto.users .
scp cse@host_name:/home/cse/auto.master .
scp cse@host_name:/home/cse/fullchain.pem .
```

## Move file 
```
mv fullchain.pem /etc/ssl/certs
mv auto* /etc
```

## Configure these two files
```
vim /etc/ldap/ldap.conf

vim /etc/nsswitch.conf
```

## Check autofs & nscd service and enable it
```
systemctl status autofs

systemctl status nscd

systemctl enable autofs

systemctl enable nscd
```