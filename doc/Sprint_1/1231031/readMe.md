## Building 4 ##

### General Information ###

- This building horizontal dimensions are, approximately, 30x30 meters.
- Both floors must have wireless LAN coverage (Wi-Fi).


## 1. Information ##

### Floor 0 ###

- The ground floor has an underfloor cable raceway connected to the external technical ditch.
- The ceiling height on this floor is 4 meters.
- Room 4.0.10 is a storage area that may be used to house a cross-connect, no network outlets are required there.
- Rooms 4.0.2 have specific purposes and the only network outlets required there are two near each floor cable passageway.
- Shared areas, like the entrance hall, restrooms, and stairs, require no network outlets.
- Elsewhere, the standard number of network outlets per area ratio is to be enforced.

### Floor 1  ###

- The ceiling height on this floor is 3 meters, however there’s a removable dropped ceiling, placed 2.5 meters from the ground, covering the entire floor.
- The space over the dropped ceiling is perfect to install cable raceways and wireless access-points.
- This floor has no underfloor cable raceways.
- Room 4.1.17 and 4.1.18 is a storage area, no network outlets are required there as well, and it may be used to house a cross-connect and other network infrastructure hardware.
- No network outlets are required at restrooms and common areas like corridors and halls.
- In every identified room, the standard number of network outlets per area rate should be honoured.


## 2. Measurements ##

**Excel with all the details about measurements**
- [Download Measurements_Building4.xlsx](Measurements_Building4.xlsx)

### Floor 0 ###

![MeasurementsBuilding4_Floor0](MeasurementsBuilding4_Floor0.png)

| Rooms  | Area in m2 | Nº outlets |
|--------|------------|------------|
| 4.0.1  | 26.9       | 6          |
| 4.0.2  | 123.2      | 12         |
| 4.0.3  | 20.4       | 4          |
| 4.0.4  | 20.4       | 4          |
| 4.0.5  | 20.4       | 4          |
| 4.0.6  | 42         | 10         |
| 4.0.7  | 20.4       | 4          |
| 4.0.8  | 20.4       | 4          |
| 4.0.9  | 43.2       | 10         |
| 4.0.10 | 11.7       | 0          |

***Total Outlets:*** 58 + 4 (Access Point)

### Floor 1 ###

![MeasurementsBuilding4_Floor1](MeasurementsBuilding4_Floor1.png)

| Rooms  | Area in m2 | Nº outlets |
|--------|------------|------------|
| 4.1.1  | 26.9       | 10         |
| 4.1.2  | 123.2      | 6          |
| 4.1.3  | 20.4       | 6          |
| 4.1.4  | 20.4       | 8          |
| 4.1.5  | 20.4       | 6          |
| 4.1.6  | 42         | 6          |
| 4.1.7  | 20.4       | 6          |
| 4.1.8  | 20.4       | 6          |
| 4.1.9  | 43.2       | 10         |
| 4.1.10 | 11.7       | 6          |
| 4.1.11 | 26.9       | 6          |
| 4.1.12 | 123.2      | 4          |
| 4.1.13 | 20.4       | 4          |
| 4.1.14 | 20.4       | 10         |
| 4.1.15 | 20.4       | 4          |
| 4.1.16 | 42         | 4          |
| 4.1.17 | 20.4       | 0          |
| 4.1.18 | 20.4       | 0          |

***Total Outlets:*** 102 + 4 (Access Point)

## 3. Structured Cabling Schematic Plan ##

### Floor 0 ###

![CableStructure_Building4_Floor1](CableStruct_Building4_Floor0.png)


### Floor 1 ###

![CableStructure_Building4_Floor1](CableStruct_Building4_Floor1.png)

## 4. Inventory ##

## ***Cables*** ##

As defined by the team in the Planning section:
- copper cables will be **Category 7 (CAT7) Copper Cables**.
- fiber cables will be **Monomode Fiber Cables**.

The maximum distance of the cables is **90 meters**.

**The Horizontal Cross-Connect (HCC) and the Consolidation Point (CP) must be placed 1.7m from the floor.** 

**The outlets must be placed 0.7m from the floor.**

These details are already included in the cable measurements.


### Floor 0 ###

***CAT7 Copper Cables:***

- From HC to CP's: 231.7m
- From CP's to Outlets: 745.2m
- From HC to Acess Point: 304.6m

Total Copper Cable Length: 1281.5m

***Monomode Fiber Cable:***

**From Outside to ICC:** 1.7m
- **From ICC to HCC (Room 4.0.10):** 0.5m

Total Fiber Cable: 2.2m



### Floor 1 ###

***CAT7 Copper Cables:***

- From HC to CP's: 132.8m
- From CP's to Outlets: 1396.32m
- From HC to Acess Point: 99.5m

Total Copper Cable Length: 1628.62m

***Monomode Fiber Cable:***

- **From ICC to HCC (Room 4.1.17):** 4.6m

Total Fiber Cable: 4.6m


## ***Patch Panels*** ##

The patch panels must comply with the cable specifications. 
Since we chose CAT7 cables, all patch panels will also be CAT7.
Similarly, as we selected Monomode Fiber Cable, the Fiber Patch Panels must be compatible with Monomode as well.

### Floor 0 ###

- 1 fiber patch panel of 12 ports (ICC)(Room 4.0.10);
- 2 patch panels of 12 ports (HCC)(Room 4.0.10)   (Copper patch panel and Fiber patch panel);
- 3 copper patch panels of 24 ports (CP's)(Rooms 4.0.9, 4.0.6, 4.0.3);

#### Total: **1 copper patch panels of 12 ports**,**1 fiber patch panel of 12 ports**  and **3 copper patch panels of 24 ports**


### Floor 1 ###

- 2 patch panels of 12 ports (HCC)(Room 4.1.17) (Copper patch panel and Fiber patch panel);
- 5 copper patch panel of 24 ports (CP's)(Room 4.1.1, 4.1.1, 4.1.9, 4.1.12, 4.1.14);

#### Total: **2 copper patch panels of 12 ports**,**2 fiber patch panel of 12 ports**  and **5 copper patch panel of 24 ports**


## ***Racks*** ##

### Floor 0 ###

For the **Intermediate Cross-Connect:**

- **1U** for 1 fiber patch panel of 12 ports;
- **1U** switch;
- **2U** an additional 100% over dimensioning.

#### **Total**: 4U

For the **Horizontal Cross-Connect:** 

- **1U** for 1 copper patch panel of 12 ports;
- **1U** for 1 fiber patch panel of 12 ports;
- **1U** switch;
- **3U** an additional 100% over dimensioning.

#### **Total**: 6U

For each of the 3 **Consolidation Point (24 ports)**

- **1U** for 1 copper patch panel of 24 ports;
- **1U** switch;
- **2U** an additional 100% over dimensioning.

#### **Total**: 4U

### Floor 1 ###


For the **Horizontal Cross-Connect:**

- **1U** for 1 copper patch panel of 12 ports;
- **1U** for 1 fiber patch panel of 12 ports;
- **1U** switch;
- **3U** an additional 100% over dimensioning.


#### **Total**: 6U

For each of the 5 **Consolidation Point (24 ports)**

- **1U** for 1 copper patch panel of 24 ports;
- **1U** switch;
- **2U** an additional 100% over dimensioning.

#### **Total**: 4U



## **TOTAL INVENTORY** ##

- Outlets: 168
- CAT7 Copper Cable (m): 2677.82
- Monomode Fiber Cable (m): 6.8
- Intermediate Cross-Connect (ICC): 1
- Horizontal Cross-Connect (HCC): 2
- Consolidation Points (CP with 24 ports): 8
- Access Point (AP): 8
- Copper Patch Panels (12 ports): 2
- Fiber Patch Panels (12 ports): 3
- Copper Patch Panels (24 ports): 8
- Telecommunications Enclosures: 11


