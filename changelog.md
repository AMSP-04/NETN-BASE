## Changelog NETN-BASE

### NETN-BASE#1 Harmonize data types
* Added datatype `ConcentrationKgPerMeterCubedFloat32`
* Added datatype `SpeedMeterPerSecondFloat32`
* Added datatype `PercentFloat64`
* Updated semantics of datatype `QuantityFloat32`
* Added datatype `QuantityFloat64`
* Added datatype `QuantityInt32`
* Renamed datatype `TimeSecInt64` to `EpochTimeSecInt64` and updated semantics for logical time
* Added datatype `TimeSecInt32`
* Added datatype `DirectionDegreesFloat32`
* Added datatype `LatLongDegreesFloat64`
* Added datatype `FederateName` (from TMR)
* Added datatype `CancellationReasonEnum32` (from TMR)
* Added datatype `TransactionId` (from ETR and TMR)
* Changed `modelIdentification` `securityClassification` from `unclassified` to `Not Classified`
* Changed `modelIdentification` `other` to include license information
* Changed `modelIdentification` `useHistory` to only include formally released versions
* Added datatype `DegreesPerSecondFloat32` 
* Added datatype `AltitudeMeterFloat64 `
* Added datatype `DraughtMeterFloat32 `
* Added datatype `IMOType `
* Added datatype `MIDType`
* Added datatype `ShipTypeType`
* Added datatype `ArrayOfStringType`

### NETN-BASE#2 Add Generic datatypes for geographical features e.g. Path datatype
* Renamed `ArrayOfWorldLocationStruct3` to `GeocentricPolygon`
* Renamed `ArrayOfWorldLocationStruct2` to `GeocentricPath`
* Added Array datatape `GeodeticPath`
* Added Array datatape `GeodeticPolygon`
* Added FixedRecord datatype `GeodeticCircle`
* Added FixedRecord datatype `GeodeticLocation`
* FixedRecord datatype `GeodeticQuadrangle`


### Changes for v.1.0.2
Version 1.0.2 was developed by MSG-106 & MSG-134 and included in NETN-FOM v2.0 and AMSP-04 Ed A.

* v1.0.0 - First version in NETN FOM v2
* v1.0.1 - Added array data type: ArrayOfWorldLocation3 (moved from NETN_Aggregate FOM module)
* v1.0.2 - Renamed data type, new name: ArrayOfWorldLocationStruct3. Updated References, Dependency
* 2020-03-18 - LO - Moved datatypes from NETN-SE to NETN-BASE
* 2020-03-19 - LO - Moved datatypes from NETN-ORG ans NETN-ETR to NETN-BASE

## Previous history
Common datatypes were defined in NETN FOM v1.0 modules NETN_AggDeagg_v1.07_2010, NETN_Service_Consumer_Provider_v1.0.3_2010 and NETN_Logistics_v1.1.2_2010.


