### IPv4 addresses to be used, and the ISP router IPv4 address ###

| Student Number | Building |     IP      |
|:--------------:|:--------:|:-----------:|
|    1231267     | Backbone | 10.23.160.0 |
|    1231267     |    1     | 10.23.162.0 |
|    1222123     |    2     | 10.23.164.0 |
|    1230927     |    3     | 10.23.168.0 |
|    1231031     |    4     | 10.23.172.0 |

# Building 1

- End user outlets on the ground floor: 40 nodes
- End user outlets on floor one: 45 nodes
- Wi-Fi network: 95 nodes
- DMZ (Servers, administration workstations, and network infrastructure devices): 110 nodes
- VoIP (IP-phones): 70 nodes

## Building 1 Networks ##

| Network                              | Number of nodes | Type of network | 
|--------------------------------------|-----------------|-----------------|
| DMZ                                  | 110             | /25             |
| Wi-Fi network                        | 95              | /25             |
| VoIP                                 | 70              | /25             |
| End user outlets on floor one        | 45              | /26             |
| End user outlets on the ground floor | 40              | /26             |

## VLANs and IP'S ##

| VLAN Location | VLAN ID | Nodes | Network IP       | Default Gateway | Network Mask    | Range Usable IP             | Available Hosts | Broadcast     | 
|:--------------|:--------|:------|:-----------------|:----------------|:----------------|:----------------------------|:----------------|---------------|
| Floor 0       | 382     | 40    | 10.23.163.192/26 | 10.23.163.193   | 255.255.255.192 | 10.23.163.193-10.23.163.254 | 62              | 10.23.163.255 |
| Floor 1       | 383     | 45    | 10.23.163.128/26 | 10.23.163.129   | 255.255.255.192 | 10.23.163.129-10.23.163.190 | 62              | 10.23.163.191 |
| Wi-Fi         | 384     | 95    | 10.23.162.128/25 | 10.23.162.129   | 255.255.255.128 | 10.23.162.129-10.23.162.254 | 126             | 10.23.162.255 |
| DMZ           | 385     | 110   | 10.23.162.0/25   | 10.23.162.1     | 255.255.255.128 | 10.23.162.1-10.23.162.126   | 126             | 10.23.162.127 |
| VoIP          | 386     | 70    | 10.23.163.0/25   | 10.23.163.1     | 255.255.255.128 | 10.23.163.1-10.23.163.126   | 126             | 10.23.163.127 |


# Router #
## Sub-Interfaces ##

|      SubInt       | VLan Id |
|:-----------------:|:-------:|
| FastEthernet1/0.1 |   383   |
| FastEthernet1/0.2 |   382   |
| FastEthernet1/0.3 |   384   |
| FastEthernet1/0.4 |   385   |
| FastEthernet1/0.5 |   386   |

# Building 2

- End user outlets on the ground floor: 110 nodes
- End user outlets on floor one: 100 nodes
- Wi-Fi network: 200 nodes
- DMZ (Servers, administration workstations, and network infrastructure devices): 60 nodes
- VoIP (IP-phones): 120 nodes


## Building 2 Networks ##
![Building2Networks](Building2_network.png)


| Network                              | Number of nodes | Type of network |
|--------------------------------------|-----------------|-----------------|
| End user outlets on the ground floor | 110             | /24             |
| End user outlets on floor one        | 100             | /25             |
| Wi-Fi network                        | 200             | /24             |
| DMZ                                  | 60              | /25             |
| VoIP                                 | 120             | /24             |


## VLANs and IP'S ##

| VLAN Location | VLAN ID | Nodes | Network IP       | Default Gateway | Network Mask     | Range Usable IP               | Available Hosts | Broadcast       | 
|:--------------|:--------|:------|:-----------------|:----------------|:-----------------|:------------------------------|:----------------|-----------------|
| Floor 0       | 388     | 110   | 10.23.166.0/24   | 10.23.166.1     | 255.255.255.0    | 10.23.166.1-10.23.166.254     | 254             | 10.23.166.255  |
| Floor 1       | 389     | 100   | 10.23.167.128/25 | 10.23.167.129   | 255.255.255.128  | 10.23.167.129-10.23.167.254   | 126             | 10.23.167.255  |
| Wi-Fi         | 390     | 200   | 10.23.165.0/24   | 10.23.165.1     | 255.255.255.0    | 10.23.165.1-10.23.165.254     | 254             | 10.23.165.255  |
| DMZ           | 391     | 60    | 10.23.167.0/25   | 10.23.167.1     | 255.255.255.128  | 10.23.167.1-10.23.167.126     | 126             | 10.23.166.127  |
| VoIP          | 392     | 120   | 110.23.164.0/24  | 110.23.164.1    | 255.255.255.0    | 110.23.164.1-110.23.164.254   | 254             | 110.23.164.255  |



# Router #
## Sub-Interfaces ##

|      SubInt       | VLan Id |
|:-----------------:|:-------:|
| FastEthernet1/0.1 |   388   |
| FastEthernet1/0.2 |   389   |
| FastEthernet1/0.3 |   390   |
| FastEthernet1/0.4 |   391   |
| FastEthernet1/0.5 |   392   |


# Building 3

- End user outlets on the ground floor: 115 nodes
- End user outlets on floor one: 135 nodes
- Wi-Fi network: 220 nodes
- DMZ (Servers, administration workstations, and network infrastructure devices): 50 nodes
- VoIP (IP-phones): 170 nodes

## Building 3 Networks ##

| Network                              | Number of nodes | Type of network | 
|--------------------------------------|-----------------|-----------------|
| Wi-Fi network                        | 220             | /24             |
| VoIP                                 | 170             | /24             |
| End user outlets on floor one        | 135             | /24             |
| End user outlets on the ground floor | 115             | /25             |
| DMZ                                  | 50              | /26             |

## VLANs and IP'S ##

| VLAN Location | VLAN ID | Nodes | Network IP       | Default Gateway | Network Mask    | Range Usable IP             | Available Hosts | Broadcast     | 
|:--------------|:--------|:------|:-----------------|:----------------|:----------------|:----------------------------|:----------------|---------------|
| Floor 0       | 393     | 115   | 10.23.171.0/25   | 10.23.171.1     | 255.255.255.128 | 10.23.171.1-10.23.171.126   | 126             | 10.23.171.127 |
| Floor 1       | 394     | 135   | 10.23.170.0/24   | 10.23.170.1     | 255.255.255.0   | 10.23.170.1-10.23.170.254   | 254             | 10.23.170.255 |
| Wi-Fi         | 395     | 220   | 10.23.168.0/24   | 10.23.168.1     | 255.255.255.0   | 10.23.168.1-10.23.168.254   | 254             | 10.23.168.255 |
| DMZ           | 396     | 50    | 10.23.171.128/26 | 10.23.171.129   | 255.255.255.192 | 10.23.171.129-10.23.171.190 | 62              | 10.23.171.191 |
| VoIP          | 397     | 170   | 10.23.169.0/24   | 10.23.169.1     | 255.255.255.0   | 10.23.169.1-10.23.169.254   | 254             | 10.23.169.255 |

# Router #
## Sub-Interfaces ##

|      SubInt       | VLan Id |
|:-----------------:|:-------:|
| FastEthernet1/0.1 |   393   |
| FastEthernet1/0.2 |   394   |
| FastEthernet1/0.3 |   395   |
| FastEthernet1/0.4 |   396   |
| FastEthernet1/0.5 |   397   |


# Building 4

- End user outlets on the ground floor: 125 nodes
- End user outlets on floor one: 170 nodes
- Wi-Fi network: 200 nodes
- DMZ (Servers, administration workstations, and network infrastructure devices): 45 nodes
- VoIP (IP-phones): 160 nodes

## Building 4 Networks ##


| Network                              | Number of nodes | Type of network | 
|--------------------------------------|-----------------|-----------------|
| Wi-Fi network                        | 200             | /24             |
| End user outlets on floor one        | 170             | /24             |
| VoIP                                 | 160             | /24             |
| End user outlets on the ground floor | 125             | /25             |
| DMZ                                  | 45              | /26             |


## VLANs and IP'S ##

| VLAN Location | VLAN ID | Nodes | Network IP       | Default Gateway | Network Mask    | Range Usable IP             | Available Hosts | Broadcast     | 
|:--------------|:--------|:------|:-----------------|:----------------|:----------------|:----------------------------|:----------------|---------------|
| Floor 0       | 398     | 125   | 10.23.175.0/25   | 10.23.175.1     | 255.255.255.128 | 10.23.175.1-10.23.175.126   | 126             | 10.23.175.127 |
| Floor 1       | 399     | 170   | 10.23.173.0/24   | 10.23.173.1     | 255.255.255.0   | 10.23.173.1-10.23.173.254   | 254             | 10.23.173.255 |
| Wi-Fi         | 400     | 200   | 10.23.172.0/24   | 10.23.172.1     | 255.255.255.0   | 10.23.172.1-10.23.172.254   | 254             | 10.23.172.255 |
| DMZ           | 401     | 45    | 10.23.175.128/26 | 10.23.175.129   | 255.255.255.192 | 10.23.175.129-10.23.175.190 | 62              | 10.23.175.191 |
| VoIP          | 402     | 160   | 10.23.174.0/24   | 10.23.174.1     | 255.255.255.0   | 10.23.174.1-10.23.174.254   | 254             | 10.23.174.255 |


# Router #
## Sub-Interfaces ##


|      SubInt       | VLan Id |
|:-----------------:|:-------:|
| FastEthernet1/0.1 |   398   |
| FastEthernet1/0.2 |   399   |
| FastEthernet1/0.3 |   400   |
| FastEthernet1/0.4 |   401   |
| FastEthernet1/0.5 |   402   |