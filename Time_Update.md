## Time Update
Step 1: Check
```
timedatectl
```
Output :-  </br>
System clock synchronized: yes </br>
NTP service: active </br>
RTC in local TZ: no


Step 2:
```
Authenticate Machine
```

Step 3: Check Status of timesyncd
```
systemctl status systemd-timesyncd

```
Step 4:
```
systemctl restart systemd-timesyncd
```
Step 5: Check
```
timedatectl
```