
# NETN-BASE
|Version| Date| Dependencies|
|---|---|---|
|3.0|2023-04-07|RPR-Base|

The NATO Education and Training Network (NETN) Base Datatypes (BASE) Module provides standard definitions of datatypes and extends the RPR-BASE FOM Module.

This module is a base module for all other NETN-FOM modules. It specifies standard data types and structures and extends the RPR-BASE module. The specification is based on IEEE 1516 High Level Architecture (HLA) Object Model Template (OMT) and supports interoperability in a federated simulation (federation) based on HLA. An HLA-based Federation Object Model (FOM) is used to specify types of data and their encoding on the network.




## Object Classes

Note that inherited and dependency attributes are not included in the description of object classes.



### HLAobjectRoot



|Attribute|Datatype|Semantics|
|---|---|---|
|UniqueId|UUID|Required. A unique identifier for the object. The Universally Unique Identifier (UUID) is generated or defined during scenario initialization.|
|FederateApplication|UUID|Optional. Reference to the federate with the main responsibility for modelling the object behaviour.|
|Time|ScenarioTime|Optional: The time in the scenario when the object is created. Scenario time is milliseconds since Epoch, where Epoch is January 1, 1970 00:00:00 UTC or otherwise defined in federation agreements.|

## Interaction Classes

Note that inherited and dependency parameters are not included in the description of interaction classes.

### HLAinteractionRoot



|Parameter|Datatype|Semantics|
|---|---|---|
|UniqueId|UUID|Optional: A unique identifier for the interaction.|
|FederateApplication|UUID|Optional. Reference to the federate application sending this interaction.|
|Time|ScenarioTime|Optional: Scenario time when the interaction was sent. Scenario time is milliseconds since Epoch, where Epoch is January 1, 1970 00:00:00 UTC or otherwise defined in federation agreements.|

## Datatypes

Note that only datatypes defined in this FOM Module are listed below. Please refer to FOM Modules on which this module depends for other referenced datatypes.

### Overview
|Name|Semantics|
|---|---|
|ActiveStatusEnum8|A state which indicates the status of an object concerning its participation in the simulation. An object in an inactive state is not simulated and does not interact with other objects.|
|AggregateMissionEnum16|A representation of the general class or nature of activity related to a simulated entity's mission.|
|AggregateStateFormationEnum32|Aggregate State-Formation [UID 205]|
|AltitudeMeterFloat64|Generic representation of altitude defined by the context of use, i.e. height Above Mean Sea Level, height Above Ground Level.|
|ArrayOfUuid|An array of Unique Identifiers expressed as UUIDs.|
|Callsign|An identifier for a simulated entity. Callsigns should be unique in the context in which they are used but are not required to be globally unique.|
|CancellationReasonEnum32|Describes the reason for cancellation.|
|DamageStatusEnhancedEnum32|The damage status of an object.|
|DamageStatusEnum32|Damaged appearance|
|DirectionDegreesFloat32|The compass direction is measured clockwise relative to the true north. Calculate values outside the range [0, 360) as modulo 360.|
|EchelonEnum32|The echelon level of a unit.|
|FederateName|The unique name of a federate participating in an HLA federation.|
|GeodeticCircle|A geodetic point and radius specifying a circle on the earth's surface (WGS84) where the radius is a great circle distance on the surface.|
|GeodeticLocation|A geodetic point, specified by latitude and longitude, with unspecified altitude. WGS84|
|GeodeticPoint|A geodetic point is specified by latitude, longitude and altitude.|
|GeodeticPolygon|A sequence of geodetic locations defines a geographical area bounded by a closed path where the first and last locations in the sequence are connected. Each point is a geodetic coordinate in WGS84 on the earth's surface, and each segment is a great circle between locations.|
|GeodeticQuadrangle|A latitude-longitude quadrangle is a region bounded by two meridians and two parallels.|
|HostilityStatusCodeEnum32|The value represents the perceived hostility status.|
|LatLongDegreesFloat64|Represents a measure of either latitude or longitude in decimal degrees of arc.|
|LocationStruct|The location of a point in space. Unless specified otherwise for the attribute, parameter, or datatype field using this datatype, the location is in the world coordinate system, as specified in IEEE Std 1278.1-2012 section 1.6.3.|
|LocationStructArray|An array of LocationStruct elements representing a path. When projected on the earth's surface, the datatype can represent an area by connecting the first and last location in the array.|
|MassConcentrationFloat32|The concentration of a substance is measured as kg/m3.|
|MassDensityFloat32|The density of a substance is measured as kg/m3.|
|QuantityFloat32|A generic floating-point quantity.|
|QuantityFloat64|A generic floating-point quantity.|
|QuantityInt32|A generic discrete quantity.|
|ScenarioTime|Scenario time is milliseconds since Epoch, where Epoch is January 1, 1970 00:00:00 UTC or otherwise defined in federation agreements.|
|SupplyStruct|The quantity of a supply type.|
|SupplyStructArray|A list of supply types and their quantity.|
|SymbolIdentifier|A symbol identifier is represented as a string. The identifier uses a URI notation (uri:xxxxxxxxxx) where the URI moniker specifies the symbology standard, e.g. app6a, app6b, app6c, 2525b, 2525c, 2525d. If not provided, the federation agreement defines the default symbol standard.|
|TimeMillisecondInt64|A generic representation of milliseconds, unit symbol ms.|
|UUID|4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs. For example, 00112233-4455-8877-6699-aabbccddeeff is encoded as the bytes 00 11 22 33 44 55 88 77 66 99 aa bb cc dd ee ff.|
        
### Simple Datatypes
|Name|Units|Semantics|
|---|---|---|
|AltitudeMeterFloat64|Meter|Generic representation of altitude defined by the context of use, i.e. height Above Mean Sea Level, height Above Ground Level.|
|DirectionDegreesFloat32|Degree|The compass direction is measured clockwise relative to the true north. Calculate values outside the range [0, 360) as modulo 360.|
|LatLongDegreesFloat64|Degree|Represents a measure of either latitude or longitude in decimal degrees of arc.|
|MassConcentrationFloat32|kg/m3|The concentration of a substance is measured as kg/m3.|
|MassDensityFloat32|kg/m3|The density of a substance is measured as kg/m3.|
|QuantityFloat32|NA|A generic floating-point quantity.|
|QuantityFloat64|NA|A generic floating-point quantity.|
|QuantityInt32|NA|A generic discrete quantity.|
|ScenarioTime|Millisecond (ms)|Scenario time is milliseconds since Epoch, where Epoch is January 1, 1970 00:00:00 UTC or otherwise defined in federation agreements.|
|TimeMillisecondInt64|Millisecond (ms)|A generic representation of milliseconds, unit symbol ms.|
        
### Enumerated Datatypes
|Name|Representation|Semantics|
|---|---|---|
|ActiveStatusEnum8|HLAoctet|A state which indicates the status of an object concerning its participation in the simulation. An object in an inactive state is not simulated and does not interact with other objects.|
|AggregateMissionEnum16|HLAinteger16BE|A representation of the general class or nature of activity related to a simulated entity's mission.|
|AggregateStateFormationEnum32|RPRunsignedInteger32BE|Aggregate State-Formation [UID 205]|
|CancellationReasonEnum32|HLAinteger32BE|Describes the reason for cancellation.|
|DamageStatusEnhancedEnum32|HLAinteger32BE|The damage status of an object.|
|DamageStatusEnum32|RPRunsignedInteger32BE|Damaged appearance|
|EchelonEnum32|HLAinteger32BE|The echelon level of a unit.|
|HostilityStatusCodeEnum32|HLAinteger32BE|The value represents the perceived hostility status.|
        
### Array Datatypes
|Name|Element Datatype|Semantics|
|---|---|---|
|ArrayOfUuid|UUID|An array of Unique Identifiers expressed as UUIDs.|
|Callsign|HLAunicodeChar|An identifier for a simulated entity. Callsigns should be unique in the context in which they are used but are not required to be globally unique.|
|FederateName|HLAunicodeChar|The unique name of a federate participating in an HLA federation.|
|GeodeticPolygon|GeodeticLocation|A sequence of geodetic locations defines a geographical area bounded by a closed path where the first and last locations in the sequence are connected. Each point is a geodetic coordinate in WGS84 on the earth's surface, and each segment is a great circle between locations.|
|LocationStructArray|LocationStruct|An array of LocationStruct elements representing a path. When projected on the earth's surface, the datatype can represent an area by connecting the first and last location in the array.|
|SupplyStructArray|SupplyStruct|A list of supply types and their quantity.|
|SymbolIdentifier|HLAunicodeChar|A symbol identifier is represented as a string. The identifier uses a URI notation (uri:xxxxxxxxxx) where the URI moniker specifies the symbology standard, e.g. app6a, app6b, app6c, 2525b, 2525c, 2525d. If not provided, the federation agreement defines the default symbol standard.|
|UUID|HLAbyte|4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs. For example, 00112233-4455-8877-6699-aabbccddeeff is encoded as the bytes 00 11 22 33 44 55 88 77 66 99 aa bb cc dd ee ff.|
        
### Fixed Record Datatypes
|Name|Fields|Semantics|
|---|---|---|
|GeodeticCircle|CenterPoint, Radius|A geodetic point and radius specifying a circle on the earth's surface (WGS84) where the radius is a great circle distance on the surface.|
|GeodeticLocation|Latitude, Longitude|A geodetic point, specified by latitude and longitude, with unspecified altitude. WGS84|
|GeodeticPoint|Latitude, Longitude, Altitude|A geodetic point is specified by latitude, longitude and altitude.|
|GeodeticQuadrangle|Point1, Point2|A latitude-longitude quadrangle is a region bounded by two meridians and two parallels.|
|LocationStruct|X, Y, Z|The location of a point in space. Unless specified otherwise for the attribute, parameter, or datatype field using this datatype, the location is in the world coordinate system, as specified in IEEE Std 1278.1-2012 section 1.6.3.|
|SupplyStruct|SupplyType, Quantity|The quantity of a supply type.|
    