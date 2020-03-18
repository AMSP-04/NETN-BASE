## Changelog NETN-BASE

### NETN-BASE#1 Harmonize data types
* Added Simple data type `ConcentrationKgPerMeterCubedFloat32`
* Added Simple data type `SpeedMeterPerSecondFloat32`
* Added Simple data type `PercentFloat64`
* Updated semantics of data type `QuantityFloat32`
* Added Simple data type `QuantityFloat64`
* Added Simple data type `QuantityInt32`
* Renamed data type `TimeSecInt64` to `EpochTimeSecInt64`
* Added data type `TimeSecInt32`
* Added data type `DirectionDegreesFloat32`
* Added data type `LatLongDegreesFloat64`
* Added datatype `FederateName` (from TMR).
* Added datatype `CancellationReasonEnum32` (from TMR).
* Added datatype `TransactionId` (from ETR and TMR).
* Changed `modelIdentification` `securityClassification` from `unclassified` to `Not Classified`
* Changed `modelIdentification` `other` to include license information
* Changed `modelIdentification` `useHistory` to only include formally relesed versions. 

### NETN-BASE#2 Add Generic datatypes for geographical features e.g. Path datatype
* Renamed `ArrayOfWorldLocationStruct3` to `GeocentricPolygon`
* Renamed `ArrayOfWorldLocationStruct2` to `GeocentricPath`
* Added Array Datatpe `GeodeticPath`
* Added Array Datatpe `GeodeticPolygon`
* Added FixedRecord Datatype `GeodeticCircle`
* Added FixedRecord Datatype `GeodeticLocation`
* FixedRecord Datatype `GeodeticQuadrangle`


### Changes for v.1.0.2
Version 1.0.2 was developed by MSG-106 & MSG-134 and included in NETN-FOM v2.0 and AMSP-04 Ed A.

* v1.0.0 - First version in NETN FOM v2
* v1.0.1 - Added array data type: ArrayOfWorldLocation3 (moved from NETN_Aggregate FOM module)
* v1.0.2 - Renamed data type, new name: ArrayOfWorldLocationStruct3. Updated References, Dependency
* 2020-03-18 - LO - Moved datatypes from NETN-SE to NETN-BASE

## Previous history
Common datatypes were defined in NETN FOM v1.0 modules NETN_AggDeagg_v1.07_2010, NETN_Service_Consumer_Provider_v1.0.3_2010 and NETN_Logistics_v1.1.2_2010.


