## Changelog NETN-BASE

### [NETN-BASE#1 Harmonize data types](https://github.com/AMSP-04/NETN-BASE/issues/1)
* Added datatype `ConcentrationKgPerMeterCubedFloat32`
* Added datatype `SpeedMeterPerSecondFloat32`
* Added datatype `PercentFloat64`
* Added datatype `QuantityFloat64`
* Added datatype `QuantityInt32`
* Added datatype `TimeSecInt32`
* Added datatype `DirectionDegreesFloat32`
* Added datatype `LatLongDegreesFloat64`
* Added datatype `FederateName`
* Added datatype `CancellationReasonEnum32`
* Added datatype `TransactionId`
* Added datatype `DegreesPerSecondFloat32` 
* Added datatype `AltitudeMeterFloat64 `
* Added datatype `DraughtMeterFloat32 `
* Added datatype `IMOType `
* Added datatype `MIDType`
* Added datatype `ShipTypeType`
* Added datatype `ArrayOfStringType`
* Added datatype `SymbolIdentifier15`
* Added datatype `SymbolIdentifier30`
* Added datatype `EchelonEnum32`
* Updated datatype `QuantityFloat32`
* Renamed & updated datatype `TimeSecInt64` to `EpochTimeSecInt64` 
* Changed `modelIdentification` `securityClassification` from `unclassified` to `Not Classified`
* Changed `modelIdentification` `other` to include license information
* Changed `modelIdentification` `useHistory` to only include formally released versions


### [NETN-BASE#2 Add Generic datatypes for geographical features e.g. Path datatype](https://github.com/AMSP-04/NETN-BASE/issues/2)
* Added datatype `GeodeticPath`
* Added datatype `GeodeticPolygon`
* Added datatype `GeodeticCircle`
* Added datatype `GeodeticLocation`
* Added datatype `GeodeticQuadrangle`
* Renamed datatype `ArrayOfWorldLocationStruct3` to `GeocentricPolygon`
* Renamed datatype `ArrayOfWorldLocationStruct2` to `GeocentricPath`

### Changes for v.1.0.2
Version 1.0.2 was developed by MSG-106 & MSG-134 and included in NETN-FOM v2.0 and AMSP-04 Ed A.

* v1.0.0 - First version in NETN FOM v2
* v1.0.1 - Added array data type: ArrayOfWorldLocation3 (moved from NETN_Aggregate FOM module)
* v1.0.2 - Renamed data type, new name: ArrayOfWorldLocationStruct3. Updated References, Dependency
* 2020-03-18 - LO - Moved datatypes from NETN-SE to NETN-BASE
* 2020-03-19 - LO - Moved datatypes from NETN-ORG ans NETN-ETR to NETN-BASE

## Previous history
Common datatypes were defined in NETN FOM v1.0 modules NETN_AggDeagg_v1.07_2010, NETN_Service_Consumer_Provider_v1.0.3_2010 and NETN_Logistics_v1.1.2_2010.


