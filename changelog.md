## Changelog NETN-BASE

### v1.0 - Initial version developed by MSG-106 and MSG-134. Release included in NETN-FOM v2.0

* v1.0.0 - First version in NETN FOM v2
* v1.0.1 - Added array data type: ArrayOfWorldLocation3 (moved from NETN_Aggregate FOM module)
* v1.0.2 - Renamed data type, new name: ArrayOfWorldLocationStruct3. Updated References, Dependency


Previous history
Common datatypes were defined in NETN FOM v1.0 modules NETN_AggDeagg_v1.07_2010, NETN_Service_Consumer_Provider_v1.0.3_2010 and NETN_Logistics_v1.1.2_2010.


### v2.0 - Updated version developed by MSG-163. Release included in NETN-FOM v3.0

* Changed `modelIdentification` `securityClassification` from `unclassified` to `Not Classified`
* Changed `modelIdentification` `other` to include license information
* Changed `modelIdentification` `useHistory` to only include formally released versions
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
* Added datatype `CancellationReasonEnum32`
* Added datatype `EchelonEnum32`
* Added datatype `EchelonEnum32`
* Added datatype `SymbolStandardEnum32`
* Added datatype `GeoLocationTypeEnum32`
* Added datatype `ArrayOfStringType`
* Added datatype `ArrayOfText64`
* Added datatype `FederateName`
* Removed datatype `ArrayOfWorldLocationStruct2` 
* Removed datatype `ArrayOfWorldLocationStruct3`
* Added datatype `GeodeticPath`
* Added datatype `GeodeticPolygon`
* Added datatype `SymbolIdentifier15`
* Added datatype `SymbolIdentifier30`
* Added datatype `Text64`
* Added datatype `TransactionId`
* Added datatype `UUID`
* Added datatype `GeocentricCircle`
* Added datatype `GeodeticCircle`
* Added datatype `GeodeticLocation`
* Added datatype `GeodeticQuadrangle`
* Added datatype `GeodeticPoint`
* Added datatype `AreaVariantStruct`
* Added datatype `PathVariantStruct`
* Added datatype `PointVariantStruct`
* Added datatype `SymbolVariantStruct`


### v2.1 - Updated version developed by MSG-191. Release included in NATO-FOM v4.0

* Added `UniqueId` attribute to extend `HLAobjectRoot` objectClass 
* Added `Status` attribute to extend `BaseEntity` objectClass 
* Added `SymbolId` attribute to extend `BaseEntity` objectClass 
* Added Enumerated Datatype `HostilityStatusCodeEnum32` moved from NETN-ORG 
* Added Enumerade Datatype `DamageStatusEnum32` a copy the same datatype in RPR FOM 2 Enumerations 
* Replaced Fixed Record datatype `NETN_SupplyStruct` with `SupplyStruct` a copy the same datatype in RPR Logistics 
* Replaced Array datatype `NETN_ArrayOfSupplyStruct` with `SupplyStructArray` a copy the same datatype in RPR Logistics 
* Removed datatype `TransactionId` and changed all dependencies to use `UUID` instead 
* Added datatype `WorldLocationStruct` for RPR-FOM v2 and RPR-FOM v3 compatibility

