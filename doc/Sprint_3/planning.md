**Sprint 3** | **Backlog**

| Tasks | Task Description                                                                                                                                                                                                                                             |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T.3.1 | Update the building1.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building one.                                                                                                   |
| T.3.2 | Update the building2.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building two.Final integration of each member’s Packet Tracer simulation into a single simulation (campus.pkt). |
| T.3.3 | Update the building3.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building three.                                                                                                 |
| T.3.4 | Update the building4.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building four.                                                                                                  |


**Sprint Master**

- João Sousa (1222123) will be the Sprint 3 Master.

## Details ## 

* **DNS Domain Name:** rcomp-24-25-dg-g1
* **DNS Local Domain:** building-X.rcomp-24-25-dg-g1
* **Unqualified DNS Domain Name:** ns.rcomp-24-25-dg-g1
* **Unqualified DNS Local Name:** ns.building-X.rcomp-24-25-dg-g1
* **HTTP Servers:** server1

Within DNS databases, **all names must be FQDN** (fully qualified domain names). Every name defined in DNS databases, on every name server, must end up with **rcomp-24-25-dg-g1**.

**X - Bulding Name (2, 3 or 4).**


## 2.1 OSPF area IDs ##

**Open Shortest Path First (OSPF)** is a pure **link-state routing protocol** that finds the best path between the source and the destination router using its own **Shortest Path First**, normally using a variant of the **Dijkstra** algorithm.

The**routing tables are not transmitted** from a router to its neighbours. Instead, each router **informs other routers about the surrounding network** (neighbour networks and available neighbour routers in each).

This results in every router **knowing the whole network infrastructure**, at that point each router can **build its own routing table**.

**OSPF area IDs** to be used in each building should be settled on the planning meeting, since **they can't be the same**.

| Student Number | Building | IP |
|:--------------:|:--------:|:--:|
|    1231267     | Backbone | 0  |
|    1231267     |    1     | 1  |   
|    1222123     |    2     | 2  |
|    1230927     |    3     | 3  |
|    1231031     |    4     | 4  |

## 2.2 VoIP

| Student Number | Building | Floor 0 | Floor 1 |
|:--------------:|:--------:|:-------:|:-------:|
|    1231267     |    1     |  1000   |  1001   |
|    1222123     |    2     |  2000   |  2001   |
|    1230927     |    3     |  3000   |  3001   |
|    1231031     |    4     |  4000   |  4001   |

## 2.3 DHCPv4 Service

A **DHCPv4 Service** (Dynamic Host Configuration Protocol) provides a way to **automatically provide and assign IP addresses, default gateways and other network parameters** to client devices.

A **DHCPv4 Service** (Dynamic Host Configuration Protocol) provides a way to **automatically provide and assign IP addresses, default gateways and other network parameters** to client devices.

| Building Name  | **Floor 0 Network** | **Floor 1 Network** | **WiFi Network** | **VoIP Network** |
|:--------------:|:-------------------:|:-------------------:|:----------------:|:----------------:|
| **Building 1** |      B1_F0_NET      |      B1_F1_NET      |     B1_WIFI      |     B1_VOIP      |
| **Building 2** |      B2_F0_NET      |      B2_F1_NET      |     B2_WIFI      |     B2_VOIP      |
| **Building 3** |      B3_F0_NET      |      B3_F1_NET      |     B3_WIFI      |     B3_VOIP      |
| **Building 4** |      B4_F0_NET      |      B4_F1_NET      |     B4_WIFI      |     B4_VOIP      |

## 2.4 DNS Domains

The **Domain Name System (DNS)** is the service behind **accessing information** online through **domain names** instead of **IP addresses**, as it is tasked with **translating domain names to IP addresses** so browsers can load Internet resources.

**General Domain Names:**

* **Highest-Level Domain**: rcomp-24-25-dg-g1
* **Server**: server1.rcomp-24-25-dg-g1
* **Web**: web.rcomp-24-25-dg-g1
* **WWW**: www.rcomp-24-25-dg-g1

| Building Name  |        **Local DNS**        |
|:--------------:|:---------------------------:|
| **Building 1** |      rcomp-22-23-da-g1      |
| **Building 2** | building2.rcomp-22-23-da-g1 |
| **Building 3** | building3.rcomp-22-23-da-g1 |
| **Building 4** | building4.rcomp-22-23-da-g1 |

| Building Name  | **DNS Server IPv4** |
|:--------------:|:-------------------:|
| **Building 1** |     10.23.162.2     |
| **Building 2** |     10.23.167.2     |
| **Building 3** |    10.23.171.130    |
| **Building 4** |    10.23.175.130    |

### 2.4.1 HTTP Domains

| Building Name  | **HTTP Server IPv4** |
|:--------------:|:--------------------:|
| **Building 1** |     10.23.162.3      |
| **Building 2** |     10.23.167.3      |
| **Building 3** |    10.23.171.131     |
| **Building 4** |    10.23.175.131     |


## 2.5 NAT

**Network Address Translation (NAT)** is a way to **map multiple local private addresses to a public one** before transferring any information, often enforced to hide said private addresses.

**NAT** also has different types:

* **Static NAT**, which always chooses **the same IP address every time**;

* **Dynamic NAT**, which **goes through a pool of public IP addresses**, which results in **getting a different address each time**.

## 2.6 Static Firewall

A **Static Firewall** works by **examining each packet** as it attempts to access a device, by looking at the **source** and **destination IP address**, to then **permit** or **reject** said packet.


# 3. Subtasks assignment #

* **1231267** - Update the building1.pkt layer three Packet Tracer simulation from the previous sprint.

* **1222123** - Update the building2.pkt layer three Packet Tracer simulation from the previous sprint. Final integration of each member's Packet Tracer simulation into a single simulation.

* **1230927** - Update the building3.pkt layer three Packet Tracer simulation from the previous sprint.

* **1231031** - Update the building4.pkt layer three Packet Tracer simulation from the previous sprint.