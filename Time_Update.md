## Time Update
Step 1: Check
```
timedatectl
```
Output :-   System clock synchronized: yes
            NTP service: active
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