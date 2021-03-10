# ms

- 10 Units Recieved  (In) 
-  2 Units Refresh   (RF) 
-  6 Units Rebuild   (RB) (2 will require new fans can be done on-site)
-  2 Units ASIC swap (RA) (2 will require 5 of 6 ASIC board swaps can be done on-site)

## Melrose Site S9 Triage Status

| Inbound Tag   | Triage | Detail                       | Stage   | In | RF | RB | RA | HW       | Logic    | BMminer |
|---------------|--------|------------------------------|---------|----|----|----|----|----------|----------|---------|
| mr01-s9-u1001 | FAN    | fan 5                        | SALVAGE | 1  |    | 1  |    | 30.0.1.3 | V1.3.58  | 2.0.0   |
| mr01-s9-u1002 | ASIC   | chain 6 - 62, 7 - 10, 8 - 63 | SALVAGE | 1  |    | 1  |    | -        | V1.3.58  | -       |
| mr01-s9-u1003 | FAN    | fan 6                        | SALVAGE | 1  |    | 1  |    | 30.0.1.3 | V1.3.58  | 2.0.0   |
| mr01-s9-u1004 | AOK    | all OK after flash           | REFRESH | 1  | 1  |    |    | 16.8.1.3 | -        | 2.0.0   |
| mr01-s9-u1005 | AOK    | all OK after flash           | REFRESH | 1  | 1  |    |    | 30.0.1.3 | V1.3.58  | 2.0.0   |
| mr01-s9-u1006 | ASIC   | chain 6 - 0, 7 - 63, 8 - 63  | SALVAGE | 1  |    | 1  |    | 16.8.1.3 | -        | 2.0.0   |
| mr01-s9-u1007 | ASIC   | chain 6 - 0, 7 - 0, 8 - 63   | SALVAGE | 1  |    | 1  |    |          | S9_V2.55 | -       |
| mr01-s9-u1008 | FAN    | 2 bad fan 5, 6               | SALVAGE | 1  |    | 1  |    | -        | S9_V2.54 | -       |
| mr01-s9-u1009 | FAN    | fan 5                        | SALVAGE | 1  |    |    |  1 | -        | S9_V2.54 | -       |
| mr01-s9-u1010 | ASIC   | chain 6 - 63, 7 - 63, 8 - 0  | SALVAGE | 1  |    |    |  1 | 30.0.1.3 | V1.3.58  | 2.0.0   |

## Melrose Site S9 Salvage Status

| Inbound Tag   | PS Tag         | Triage | Stage   | Tag Chain 6      | Tag Chain 7      | Tag Chain 8      | Detail                       |  | Fan 5 | Fan 6 |
|---------------|----------------|--------|---------|------------------|------------------|------------------|------------------------------|--|-------|-------|
| mr01-s9-u1001 | mr01-s9-ps1001 | FAN    | SALVAGE | mr01-s9-u1001-c6 | mr01-s9-u1001-c7 | mr01-s9-u1001-c8 | fan 5                        |  | 1     | 0     |
| mr01-s9-u1002 | mr01-s9-ps1002 | ASIC   | SALVAGE | mr01-s9-u1002-c6 | mr01-s9-u1002-c7 | mr01-s9-u1002-c8 | chain 6 - 62, 7 - 10, 8 - 63 |  | 0     | 0     |
| mr01-s9-u1003 | mr01-s9-ps1003 | FAN    | SALVAGE | mr01-s9-u1003-c6 | mr01-s9-u1003-c7 | mr01-s9-u1003-c8 | fan 6                        |  | 1     | 0     |
| mr01-s9-u1004 | mr01-s9-ps1004 | AOK    | REFRESH | na               | na               | na               | all OK after flash           |  | 0     | 0     |
| mr01-s9-u1005 | mr01-s9-ps1005 | AOK    | REFRESH | na               | na               | na               | all OK after flash           |  | 0     | 0     |
| mr01-s9-u1006 | mr01-s9-ps1006 | ASIC   | SALVAGE | mr01-s9-u1006-c6 | mr01-s9-u1006-c7 | mr01-s9-u1006-c8 | chain 6 - 0, 7 - 63, 8 - 63  |  | 0     | 0     |
| mr01-s9-u1007 | mr01-s9-ps1007 | ASIC   | SALVAGE | mr01-s9-u1007-c6 | mr01-s9-u1007-c7 | mr01-s9-u1007-c8 | chain 6 - 0, 7 - 0, 8 - 63   |  | 0     | 0     |
| mr01-s9-u1008 | mr01-s9-ps1008 | FAN    | SALVAGE | mr01-s9-u1008-c6 | mr01-s9-u1008-c7 | mr01-s9-u1008-c8 | 2 bad fan 5, 6               |  | 1     | 1     |
| mr01-s9-u1009 | mr01-s9-ps1009 | FAN    | SALVAGE | mr01-s9-u1009-c6 | mr01-s9-u1009-c7 | mr01-s9-u1009-c8 | fan 5                        |  | 1     | 0     |
| mr01-s9-u1010 | mr01-s9-ps1010 | ASIC   | SALVAGE | mr01-s9-u1010-c6 | mr01-s9-u1010-c7 | mr01-s9-u1010-c8 | chain 6 - 63, 7 - 63, 8 - 0  |  | 0     | 0     |

## Melrose Site S9 Returned Status

| Inbound Tag   | triage detail                | triage stage | Required service   | Status        | discription                                             |
|---------------|------------------------------|--------------|--------------------|---------------|---------------------------------------------------------|
| mr01-s9-u1001 | fan 5                        | SALVAGE      | fan 5              | onsite repair | suggest repair                                          |
| mr01-s9-u1002 | chain 6 - 62, 7 - 10, 8 - 63 | SALVAGE      | ASIC 6,7           | AOK           | salvaged boards 6,7 from machine u1010                  |
| mr01-s9-u1003 | fan 6                        | SALVAGE      | fan 6              | onsite repair | suggest repair                                          |
| mr01-s9-u1004 | all OK after flash           | REFRESH      | None               | AOK           | AOK                                                     |
| mr01-s9-u1005 | all OK after flash           | REFRESH      | None               | AOK           | AOK                                                     |
| mr01-s9-u1006 | chain 6 - 0, 7 - 63, 8 - 63  | SALVAGE      | ASIC 6             | AOK           | swapped board 6 and board 8 from machine u1007          |
| mr01-s9-u1007 | chain 6 - 0, 7 - 0, 8 - 63   | SALVAGE      | ASIC 6,7, 8        | salvage       | combined working boards with unit u1006 all bad in 1007 |
| mr01-s9-u1008 | 2 bad fan 5, 6               | SALVAGE      | fan 5,6            | onsite repair | suggest repair                                          |
| mr01-s9-u1009 | fan 5                        | SALVAGE      | fan 5              | onsite repair | suggest repair                                          |
| mr01-s9-u1010 | chain 6 - 63, 7 - 63, 8 - 0  | SALVAGE      | fan 5,6 ASIC 6,7,8 | salvage       | suggest salvage                                         |

updated [...](https://docs.google.com/spreadsheets/d/1_iXF0iPXyzejxnkqlGtTSFHLRK9yXqTdz1O6_KCGxH0/edit#gid=108511430) 2021.03.09 cat
