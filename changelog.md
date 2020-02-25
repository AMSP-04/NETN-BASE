## Changelog NETN-BASE

### Added datatype
ArrayOfWorldLocationStruct2 added, used by NETN-ETR and NETN-SE.

### NETN-MRM#4 Make MRM not depend on TMR
* Added datatype `FederateName` (from TMR).
* Added datatype `CancellationReasonEnum32` (from TMR).

### Changes for v.1.x (RC 1)
Version 1.X was UPDATED by MSG-163 and included in NETN-FOM v3.0 and AMSP-04 Ed B.

* Added datatype `TransactionId` (from ETR and TMR).
* Change `modelIdentification` `securityClassification` from `unclassified` to `Not Classified`
* Change `modelIdentification` `other` to include license information
* Clean-up `modelIdentification` `useHistory` to only include formally relesed versions. 


### Changes for v.1.0.2
Version 1.0.2 was developed by MSG-106 & MSG-134 and included in NETN-FOM v2.0 and AMSP-04 Ed A.

* v1.0.0 - First version in NETN FOM v2
* v1.0.1 - Added array data type: ArrayOfWorldLocation3 (moved from NETN_Aggregate FOM module)
* v1.0.2 - Renamed data type, new name: ArrayOfWorldLocationStruct3. Updated References, Dependency

## Previous history
Common datatypes were defined in NETN FOM v1.0 modules NETN_AggDeagg_v1.07_2010, NETN_Service_Consumer_Provider_v1.0.3_2010 and NETN_Logistics_v1.1.2_2010.


