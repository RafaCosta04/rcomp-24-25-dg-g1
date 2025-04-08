# IPv4 Addressing and Static Routing Report

## 1. Introduction
This document describes the planning and implementation process of IPv4 addressing and static routing configurations for Sprint 2 of the campus network simulation.

## 2. IPv4 Network Addressing

### 2.1. General Address Space

- **Allocated IPv4 Address Space:** `10.23.160.0/20`

### 2.2. Subnet Allocation Per Building

| Network        | Range Start    | Range End       | Usable IPs  |
|----------------|----------------|-----------------|-------------|
| Backbone       | 10.23.160.0    | 10.23.161.255   | 510         |
| Building 1     | 10.23.162.0    | 10.23.163.255   | 510         |
| Building 2     | 10.23.164.0    | 10.23.167.255   | 1022        |
| Building 3     | 10.23.168.0    | 10.23.171.255   | 1022        |
| Building 4     | 10.23.172.0    | 10.23.175.255   | 1022        |

Each building's subnet was further divided for specific VLANs, such as OUTLET FLOOR 0, OUTLET FLOOR 1, Wi-Fi, VOIP, DMZ.

### 2.3. IPv4 Networking Strategy For Each Building 
  
- Steps:

    - Network address blocks were assigned by identifying the number of hosts required per network.
    - Identifying the network prefix for each network.
    - Subnetting was done from the largest required subnets (smallest prefix) to the smallest (biggest prefix).
    - Care was taken to avoid any address overlap.


### 2.4. Backbone Router Assignments

| Router | IPv4 Address   |
|--------|----------------|
| MC     | 10.23.160.1    |
| B1     | 10.23.160.10   |
| B2     | 10.23.160.20   |
| B3     | 10.23.160.30   |
| B4     | 10.23.160.40   |

## 3. Static Routing

Each building router (Building 1 to Building 4) is connected to the main campus router via the 10.23.160.0/23 backbone network. 
Static routes are used to direct all external traffic to the campus core router (Router_MC) located at 10.23.160.1. 
This ensures that all inter-building and internet-bound traffic flows through a centralized point, simplifying route management and network security.


### 3.1. Router_MC Configuration
Below is the routing configuration for the MC router, which connects to the ISP and all buildings.

```bash
! Routes to Building 1
ip route 10.23.163.192 255.255.255.192 10.23.160.10
ip route 10.23.163.128 255.255.255.192 10.23.160.10
ip route 10.23.162.128 255.255.255.128 10.23.160.10
ip route 10.23.162.0 255.255.255.128 10.23.160.10
ip route 10.23.163.0 255.255.255.128 10.23.160.10

! Routes to Building 2
ip route 10.23.167.128 255.255.255.128 10.23.160.20
ip route 10.23.167.0 255.255.255.128 10.23.160.20
ip route 10.23.166.0 255.255.255.0 10.23.160.20
ip route 10.23.165.0 255.255.255.0 10.23.160.20
ip route 10.23.164.0 255.255.255.0 10.23.160.20

! Routes to Building 3
ip route 10.23.171.128 255.255.255.192 10.23.160.30
ip route 10.23.171.0 255.255.255.128 10.23.160.30
ip route 10.23.170.0 255.255.255.0 10.23.160.30
ip route 10.23.169.0 255.255.255.0 10.23.160.30
ip route 10.23.168.0 255.255.255.0 10.23.160.30

! Routes to Building 4
ip route 10.23.175.128 255.255.255.192 10.23.160.40
ip route 10.23.175.0 255.255.255.128 10.23.160.40
ip route 10.23.174.0 255.255.255.0 10.23.160.40
ip route 10.23.173.0 255.255.255.0 10.23.160.40
ip route 10.23.172.0 255.255.255.0 10.23.160.40

! Default route to ISP
ip route 0.0.0.0 0.0.0.0 87.5.127.173
```


### 3.2. Building Routers Configuration

---

### 🏢 **Router B1** - Building 1

**Interface Configurations:**
```bash
FastEthernet1/0      -> 10.23.160.10/23          (Backbone connection)
FastEthernet1/0.1    -> VLAN 383 (Floor 1)       -> 10.23.163.129/26
FastEthernet1/0.2    -> VLAN 382 (Floor 0)       -> 10.23.163.193/26
FastEthernet1/0.3    -> VLAN 384 (WiFi)          -> 10.23.162.129/25
FastEthernet1/0.4    -> VLAN 385 (DMZ)           -> 10.23.162.1/25
FastEthernet1/0.5    -> VLAN 386 (VoIP)          -> 10.23.163.1/25
```

**Static Route:**
```bash
ip route 0.0.0.0 0.0.0.0 10.23.160.1
```
➡️ All unknown destinations are routed to the main router.

---

### 🏢 **Router B2** - Building 2

**Interface Configurations:**
```bash
FastEthernet1/0      -> 10.23.160.20/23          (Backbone connection)
FastEthernet1/0.1    -> VLAN 388 (Floor 0)       -> 10.23.166.1/24
FastEthernet1/0.2    -> VLAN 389 (Floor 1)       -> 10.23.167.129/25
FastEthernet1/0.3    -> VLAN 390 (WiFi)          -> 10.23.165.1/24
FastEthernet1/0.4    -> VLAN 391 (DMZ)           -> 10.23.167.1/25
FastEthernet1/0.5    -> VLAN 392 (VoIP)          -> 10.23.164.1/24
```

**Static Route:**
```bash
ip route 0.0.0.0 0.0.0.0 10.23.160.1
```
➡️ All unknown destinations are routed to the main router.


---

### 🏢 **Router B3** - Building 3

**Interface Configurations:**
```bash
FastEthernet1/0      -> 10.23.160.30/23          (Backbone connection)
FastEthernet1/0.1    -> VLAN 393 (Floor 0)       -> 10.23.171.1/25
FastEthernet1/0.2    -> VLAN 394 (Floor 1)       -> 10.23.170.1/24
FastEthernet1/0.3    -> VLAN 395 (WiFi)          -> 10.23.168.1/24
FastEthernet1/0.4    -> VLAN 396 (DMZ)           -> 10.23.171.129/26
FastEthernet1/0.5    -> VLAN 397 (VoIP)          -> 10.23.169.1/24
```

**Static Route:**
```bash
ip route 0.0.0.0 0.0.0.0 10.23.160.1
```
➡️ All unknown destinations are routed to the main router.

---

### 🏢 **Router B4** - Building 4

**Interface Configurations:**
```bash
FastEthernet1/0      -> 10.23.160.40/23          (Backbone connection)
FastEthernet1/0.1    -> VLAN 398 (Floor 0)       -> 10.23.175.1/25
FastEthernet1/0.2    -> VLAN 399 (Floor 1)       -> 10.23.173.1/24
FastEthernet1/0.3    -> VLAN 400 (WiFi)          -> 10.23.172.1/24
FastEthernet1/0.4    -> VLAN 401 (DMZ)           -> 10.23.175.129/26
FastEthernet1/0.5    -> VLAN 402 (VoIP)          -> 10.23.174.1/24
```

**Static Route:**
```bash
ip route 0.0.0.0 0.0.0.0 10.23.160.1
```
➡️ All unknown destinations are routed to the main router.

---

### 3.3. Notes
- Each building router is responsible for routing internally within the building.
- Router_MC acts as the distributor.


## 4. Conclusion
The IPv4 addressing plan was carefully created to ensure non-overlapping networks and scalability. Static routes were manually added to the main router to allow full connectivity between all subnets.



