# S9 Processing steps
To maximize overall server farm efficiencies, ASIC Forge uses specific S9 server inbound testing process to identify problem servers and subcomponents.
Futher ASIC Forge repair and testing will identify faulty subcomponents with the goal to maximize the precentage of overall fleet efficiencies.

- S9 __Triage__
- S9 __Refresh__
- S9 __Salvage__
- S9 __Rebuild__
- S9 __ASIC Repair__

## S9 Triage Process
All inbound servers go through an initial triage consisting of the following workflow:

| Step | Sub | Detail                                                                                                                       |
|------|-----|------------------------------------------------------------------------------------------------------------------------|
| 1    |     | Label S9 unit with Triage Tag (src-s9-w<inbound serial number>).  Label Powersupply (scr-s9-ps<inbound serial number>) |
| 2    |     | Power Unit up in Triage Station                                                                                        |
| 3    |     | Obtain IP from DHCP server and access WEB                                                                              |
|      | 3.1 | If no IP is obtained mark as DOA and place into SALVAGE                                                                |
|      | 3.2 | Update Miner Configuration and Worker node info (hash to test address and rename Miner)                                |
|      | 3.3 | Record crs-s9-w<inbound serial number log>                                                                             |
| 4    |     | If controller board does not come up (start to remove possible power faults)                                           |
|      | 4.1 | Unplug power from hashboards                                                                                           |
|      | 4.2 | Unplug fans from controller board                                                                                      |
|      | 4.3 | Unplug and remove powersupply                                                                                          |
|      | 4.4 | Mark label on powersupply as "Bad" with date                                                                           |
|      | 4.5 | Attach small good powersupply to controller board and attempt Step #3 to verify good controllerboard                   |
|      | 4.6 | If Step #3 fails, tag unit as SALVAGE                                                                                  |
| 5    |     | Attach know good full powersupply and power up and evaluate unit                                                       |
  
### S9 Server status codes

- __DOA__  Unit did not pass Step 3 put through SALVAGE to identify issues and recycle good parts into rebuild 
- __WEB__  Unit gets DHCP and WEB but no FAN or HASH status                                                                                        
- __FAN__  Unit reports FAN issues Write FAN on label and TestStatus Spreadsheet                                                                   
- __ASIC__ Unit has ASIC failures. Write ASIC Chain # and ASICs Found on label and TestStatus Spreadsheet                                          
- __AOK__  Unit reports all 189 ASICS and starts to hash.  Write AOK on label and TestStatus Spreadsheet and place into REFRESH      

## S9 Refresh Process

| Step | Detail                                               |
|------|------------------------------------------------------|
| 1    | Disassemble unit                                     |
| 2    | Use compressed air to blow off dust on fans          |
| 3    | Use compressed air to blow off dust around heatsinks |
| 4    | Use alcohol to clean off boards and cables           |
| 5    | Reassemble unit                                      |
| 6    | Retest to verify AOK                                 |

## S9 Salvage Process

| Step |      |                                                                                        |
|------|------|----------------------------------------------------------------------------------------|
| 1    |      | Disassemble unit                                                                       |
| 2    |      | Separate components                                                                     |
|      | FAN  | Fans you can leave plates and screens on just remove 4 screws at corner of metal plate |
|      | CTRL | Remove Logic Controller from Chassis                                                    |
|      | ASIC | Remove ASIC hash boards from Chassis                                                   |
| 3    |      | Label and put components into the associated component test rig                          |

## S9 Rebuild

| Step | Detail                                                                                            |
|------|---------------------------------------------------------------------------------------------------|
| 1    | Assemble unit with GOOD Salvage parts logging assembled parts under inventory tag on logic board. |
| 2    | Return unit to Triage Test Process                                                                |

## S9 ASIC Repair

| Step | Detail                                                |
|------|-------------------------------------------------------|
| 1    | Identify ASIC chain break position                    |
| 2    | Remove and inspect ASIC at break position             |
| 3    | Replace / Repair defects                              |
| 4    | Retest ASIC chain                                     |
| 5    | GoTo Step 1 if ASIC chain is less than 63 and repeat  |
