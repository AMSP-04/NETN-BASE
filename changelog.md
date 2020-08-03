## Changelog NETN-BASE

### Changes for v2.0
Version 2.0 was developed by MSG-163 and included in NETN-FOM v3.0.

* Changed `modelIdentification` `securityClassification` from `unclassified` to `Not Classified`
* Changed `modelIdentification` `other` to include license information
* Changed `modelIdentification` `useHistory` to only include formally released versions

#### Simple Datatypes
* Added datatype `AltitudeMeterFloat64`
* Added datatype `DegreesPerSecondFloat32` 
* Added datatype `DirectionDegreesFloat32`
* Added datatype `DraughtMeterFloat32`
* Modified datatype `TimeSecInt64` to `EpochTimeSecInt64` 
* Added datatype `IMOType`
* Added datatype `LatLongDegreesFloat64`
* Added datatype `MassConcentrationFloat32`
* Added datatype `MassDensityFloat32`
* Added datatype `MIDType`
* Added datatype `PercentFloat64`
* Updated datatype `QuantityFloat32`
* Added datatype `QuantityFloat64`
* Added datatype `QuantityInt32`
* Added datatype `ShipTypeType`
* Added datatype `TimeSecInt32`

#### Enumerated Datatypes

* Added datatype `CancellationReasonEnum32`
* Added datatype `EchelonEnum32`

#### Array Datatypes

* Added datatype `ArrayOfStringType`
* Added datatype `FederateName`
* Modified datatype `ArrayOfWorldLocationStruct2` to `GeocentricPath`
* Modified datatype `ArrayOfWorldLocationStruct3` to `GeocentricPolygon`
* Added datatype `GeodeticPath`
* Added datatype `GeodeticPolygon`
* Added datatype `SymbolIdentifier15`
* Added datatype `SymbolIdentifier30`
* Added datatype `TransactionId`
* Added datatype `UUID`

#### Fixed Record Datatypes
* Added datatype `GeocentricCircle`
* Added datatype `GeodeticCircle`
* Added datatype `GeodeticLocation`
* Added datatype `GeodeticQuadrangle`

#### Variant Record Datatypes
* Added datatype `AreaVariantStruct`
* Added datatype `PathVariantStruct`
* Added datatype `PointVariantStruct`



### Changes for v1.0.2
Version 1.0.2 was developed by MSG-106 & MSG-134 and included in NETN-FOM v2.0.

* v1.0.0 - First version in NETN FOM v2
* v1.0.1 - Added array data type: ArrayOfWorldLocation3 (moved from NETN_Aggregate FOM module)
* v1.0.2 - Renamed data type, new name: ArrayOfWorldLocationStruct3. Updated References, Dependency


## Previous history
Common datatypes were defined in NETN FOM v1.0 modules NETN_AggDeagg_v1.07_2010, NETN_Service_Consumer_Provider_v1.0.3_2010 and NETN_Logistics_v1.1.2_2010.


