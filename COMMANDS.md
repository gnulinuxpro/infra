#### [03. L2 - VLAN](03._L2_-_VLAN.md)

```
nmcli con add type vlan con-name vlan2 dev enp0s3 id 2
```

#### [04. L2 - Агрегирование каналов](04._L2_-_Агрегирование_каналов.md)

```
nmcli con sh
nmcli con del con1 con2
nmcli con add type team con-name teams3s8 ifname team0 team.runner lacp
nmcli con add type team-slave ifname enp0s3 master team0
nmcli con add type team-slave ifname enp0s8 master team0
```
