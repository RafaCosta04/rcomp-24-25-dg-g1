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

|           SubInt           | VLan Id |
|:--------------------------:|:-------:|
|     FastEthernet0/0.1      |      |
|     FastEthernet0/0.2      |      |
|     FastEthernet0/0.3      |      |
|     FastEthernet0/0.4      |      |
|     FastEthernet0/0.5      |      |
|     FastEthernet0/0.6      |      |


# Building 3

- End user outlets on the ground floor:  nodes
- End user outlets on floor one:  nodes
- Wi-Fi network:  nodes
- DMZ (Servers, administration workstations, and network infrastructure devices):  nodes
- VoIP (IP-phones):  nodes

## Building 3 Networks ##
## VLANs and IP'S ##
# Router #
## Sub-Interfaces ##
# Building 4

- End user outlets on the ground floor:  nodes
- End user outlets on floor one:  nodes
- Wi-Fi network:  nodes
- DMZ (Servers, administration workstations, and network infrastructure devices):  nodes
- VoIP (IP-phones):  nodes

## Building 4 Networks ##
## VLANs and IP'S ##
# Router #
## Sub-Interfaces ##