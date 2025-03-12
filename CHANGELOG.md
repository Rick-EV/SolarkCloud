### 2025/03/12
Version"2.1.18.1
Correction of API call link and data queue.

### 2025/03/11
Version "2.1.18" - Added more entities
Load UPS PowerL1
Load UPS PowerL2
Load UPS PowerL3
Load UPS Total Power
-Check for a valid solark token before fetching data.
-Added Phase 2 and 3 for load
-Corrected PV3 and PV4 Voltage, Power & Current mapping.

### 2024/11/14
Version "2.1.17" - Added more entities: 
Load UPS PowerL1,
Load UPS PowerL2,
Load UPS PowerL3,
Load UPS Total Power.
Bug Fix Correcting syntax error.

### 2024/11/06
Version "2.1.16.6" - This update focuses on refining the entity naming convention for some sensor elements recently included. This ensures consistent, clear, and intuitive naming for all sensors.

### 2024/11/06
Version "2.1.16.5" - Extended entities to support 3 phase grid/inverter and added 2 extra MPPTs
The following entities were added.
Grid Phase - Power, Voltage, Current 
Grid Phase1 - Power, Voltage, Current 
Grid Phase2 - Power, Voltage, Current
Inverter Phase - Power, Voltage, Current 
Inverter Phase1 - Power, Voltage, Current 
Inverter Phase2 - Power, Voltage, Current
PV MPPT3 and PV MPPT4

### 2024/10/13
Version "2.1.16" - Added MPPT 3 & 4
Added Voltage line 2 or L2 which was not being displayed on the flow card
Updated local griddata.json to reflect Sol-Ark voltage properly
Battery 1 Charge Voltage was incorrectly mapped defaulting to 0 (Will possibly be deleted in future)
Battery Discharge Voltage 2 was never mapped from the start. (New Entity Added)
SPECIAL NOTE: Expect more issues on secondary batteries, due to limited hardware access for development some values are incorrectly assumed.
