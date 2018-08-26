---
title: ubiquiti 
---

# networks

| Name           | Purpose   | Network Group | Port  | Subnet           | VLAN |
|---             |---        |---            |---    |---               |---   |
| Cable WLAN     | WAN       | WAN1          | WAN1  |                  |      |
| 4G WLAN        | WAN       | WAN2          | WAN2  |                  |      |
| Infrastructure | Corporate | LAN           | LAN 1 | 192.168.1.1 /24  |      |
| Family         | Corporate | LAN           | LAN 1 | 10.0.10.1 /24    | 10   |
| Guest          | Corporate | LAN           | LAN 1 | 10.0.20.1 /24    | 20   |
| Homelab        | Corporate | LAN           | LAN 1 | 10.0.30.1 /24    | 30   |
| IoT            | Corporate | LAN           | LAN 1 | 10.0.40.1 /24    | 40   |
| DMZ            | Corporate | LAN           | LAN 1 | 10.0.50.1 /24    | 50   |

# firewall
- In firewall rules are processed for packets entering a given interface.
- Out firewall rules are processed for packets exiting a given interface.
- Local firewall rules are processed for packets destined for the router itself from a given interface.

![](https://community.ubnt.com/t5/image/serverpage/image-id/65938iBBDF7A4506C545AA/image-size/original)


# vlan
- https://community.ubnt.com/t5/UniFi-Routing-Switching/A-non-expert-Guide-to-VLAN-and-Trunks-in-Unifi-Switches/td-p/1804481
- https://community.ubnt.com/t5/EdgeRouter/Home-Setup-with-4-VLANs-and-Zone-Based-Firewall-ZBF/td-p/2285642

# chromecast and google home
- https://community.ubnt.com/t5/UniFi-Wireless/Chromecast-on-Guest-Network/td-p/1520187
- https://help.ubnt.com/hc/en-us/articles/360001004034-UniFi-Best-Practices-for-Managing-Chromecast-Google-Home-on-UniFi-Network
