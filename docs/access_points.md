# Access Points in Packet Tracer

In Cisco Packet Tracer, APs can only be configured visually.
This document aims to collect the configuration steps and
options needed for spaceone-corp's Access Points.

## Wiring

Access Points should be plugged into the interface f0/24 of any
desired Access Switch, but any interface is possible. Make sure
you mark the interface on the Access Switch as a VLAN 2 port
using the following commands:

```cisco
vlan 2
  name wifi

interface f0/24
  switchport mode access
  switchport access vlan 2
  no shutdown
  exit
```

Ideally, you also make sure that the range of interfaces for the access layer VLAN
(e.g. VLAN 3 for the research area) excludes the interface where the AP is wired to.

## Configuration

Go to `AP > Config > INTERFACES > Port 1` and set the following settings:

1. SSID:                    spaceone-corp.com
2. 2.4 GHz Channel:         6
3. Coverage Range (meters): 140.00
4. Authentiation:           WPA2-PSK
5. PSK Pass Phrase:         bh3ab
6. Encryption Type:         AES
