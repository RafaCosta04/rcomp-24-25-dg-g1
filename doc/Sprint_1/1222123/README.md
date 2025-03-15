## Building 2 ##

### General Information ###

- This building horizontal dimensions are, approximately, 20x40 meters.
- Both floors must have wireless LAN coverage (Wi-Fi).

## 1. Information ##

### Floor 0 ###

- The ceiling height on this floor is 4 meters.
- Common areas, like the entrance hall, restrooms, and stairs, require no network outlets.
- Rooms 2.0.6 and 2.0.7 have specific
  purposes and the only network outlets required there are 5 near each floor cable passageway.
- Room 2.0.11 is a storage area, no network outlets are
  required there as well, and it may be used to house a cross-connect and other network infrastructure
  hardware.
- In every identified room, the standard number of network outlets per area rate should be honoured.


### Floor 1  ###

- The ceiling height on this floor is 3 meters, however there’s a removable dropped ceiling, placed 2.5 meters from the ground, covering the entire floor.
- The space over the dropped ceiling is perfect to install cable raceways and wireless access-points.
- No network outlets are required at restrooms and common areas like corridors and halls.
- Room 2.1.12 is a storage area, no network outlets are
  required there as well, and it may be used to house a cross-connect and other network infrastructure
  hardware.
- In every identified room, the standard number of network outlets per area rate should be honoured.


## 2. Measurements ##

**Excel with all the details about measurements**
- [Download Measurements_Building2.xlsx](Measurements_Building2.xlsx)

### Floor 0 ###

![measurements_building2_floor0](measurements_building2_floor0.png)

| Rooms  | Area in m2 | Nº outlets |
|--------|------------|------------|
| 2.0.1  | 29,70      | 6          |
| 2.0.2  | 29,70      | 6          |
| 2.0.3  | 19,14      | 4          |
| 2.0.4  | 19,14      | 4          |
| 2.0.5  | 53,00      | 12         |
| 2.0.6  | 93,50      | 5          |
| 2.0.7  | 93,50      | 5          |
| 2.0.8  | 28,05      | 6          |
| 2.0.9  | 28,05      | 6          |
| 2.0.10 | 15,52      | 4          |
***Total Outlets:*** 58

### Floor 1 ###

![measurements_building2_floor1](measurements_building2_floor1.png)

| Room   | Area in m2 | Nº outlets |
|--------|-----------|------------|
| 2.1.1  | 26,91     | 6          |
| 2.1.2  | 25,53     | 6          |
| 2.1.3  | 25,53     | 6          |
| 2.1.4  | 25,53     | 6          |
| 2.1.5  | 25,53     | 6          |
| 2.1.6  | 17,25     | 4          |
| 2.1.7  | 30,36     | 8          |
| 2.1.8  | 30,36     | 8          |
| 2.1.9  | 30,36     | 8          |
| 2.1.10 | 30,36     | 8          |
| 2.1.11 | 28,98     | 6          |
| 2.1.13 | 17,25     | 4          |
| 2.1.14 | 30,36     | 8          |
| 2.1.15 | 46,23     | 10         |

***Total Outlets:*** 94

## 3. Structured Cabling Schematic Plan ##

### Floor 0 ###

![CableStructure_Building2_Floor1](cabling_building2_floor0.png)


### Floor 1 ###

![CableStructure_Building2_Floor1](cabling_building2_floor1.png)

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

- From HC to CP's: 132,48m
- From CP's to Outlets: 649,28m
- From HC to Acess Point: 58m

Total Copper Cable Length: 839.76m

***Monomode Fiber Cable:***

**From ICC to Outside:** 9.97m
- **From ICC to HCC (Room 2.0.11):** 1m

Total Fiber Cable: 10.97m


### Floor 1 ###

***CAT7 Copper Cables:***

- From HC to CP's: 529,28m
- From CP's to Outlets: 882,8m
- From HC to Acess Point: 53,27m

Total Copper Cable Length: 1465,35m

***Monomode Fiber Cable:***

- **From ICC to HCC (Room 2.1.12):** 6,6m

Total Fiber Cable: 6,6m

## ***Patch Panels*** ##

The patch panels must comply with the cable specifications.
Since we chose CAT7 cables, all patch panels will also be CAT7.
Similarly, as we selected Monomode Fiber Cable, the Fiber Patch Panels must be compatible with Monomode as well.

### Floor 0 ###

- 1 fiber patch panel of 12 ports (ICC)(Room 2.0.11);
- 1 copper patch panel of 12 ports (HCC)(Room 2.0.11);
- 1 fiber patch panel of 12 ports (ICC)(Room 2.0.11);
- 1 patch panel of 12 ports (CP)(Room 2.0.6);
- 3 patch panels of 24 ports (CP's)(Rooms 2.0.3, 2.0.5, 2.0.9);

#### Total: **3 patch panels of 12 ports** and **3 patch panels of 24 ports** and **2 fiber patch panels of 12 ports**


### Floor 1 ###

- 1 fiber patch panel of 12 ports (MCC)(Room 2.1.12); 
- 1 copper patch panel of 12 ports (HCC)(Room 2.1.12);
- 1 copper patch panel of 12 ports (CP)(Room 2.1.15);
- 6 copper patch panels of 24 ports (CP's)(Rooms 2.1.2, 2.1.4, 2.1.7, 2.1.9, 2.1.11, 2.1.14);

#### Total: **2 copper patch panels of 12 ports** and **6 copper patch panels of 24 ports** and **1 fiber patch panel of 12 ports** 


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

For each of the 1 **Consolidation Point (12 ports)**

- **1U** for 1 copper patch panel of 12 ports;
- **1U** switch;
- **2U** an additional 100% over dimensioning.

#### **Total**: 4U

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

For each of the 1 **Consolidation Point (12 ports)**

- **1U** for 1 copper patch panel of 12 ports;
- **1U** switch;
- **2U** an additional 100% over dimensioning.

#### **Total**: 4U

For the 6 **Consolidation Point (24 ports)**

- **1U** for 1 copper patch panel of 24 ports;
- **1U** switch;
- **2U** an additional 100% over dimensioning.

#### **Total**: 4U

## **TOTAL INVENTORY** ##

- Outlets: 152 + 4 Access Points
- CAT7 Copper Cable (m): 2305,11
- Monomode Fiber Cable (m): 17,57
- Intermediate Cross-Connect (ICC): 1
- Horizontal Cross-Connect (HCC): 2
- Consolidation Points (CP): 11
- Access Point (AP): 4
- Copper Patch Panels (12 ports): 5
- Copper Patch Panels (24 ports): 9
- Fiber Patch Panels (12 ports): 3
- Telecommunication enclosures: 14 