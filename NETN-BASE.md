# NETN-BASE
NATO Education and Training Network (NETN) Base Datatypes (BASE) Module. 
        
This module is a base module for all other NETN-FOM modules. It specifies common datatypes and structures and extends the RPR-BASE module. The specification is based on IEEE 1516 High Level Architecture (HLA) Object Model Template (OMT) and primarily intended to support interoperability in a federated simulation (federation) based on HLA. An HLA OMT based Federation Object Model (FOM) is used to specify types of data and how it is encoded on the network. The NETN-BASE FOM module is available as an XML file for use in HLA based federations.
        
## Purpose
The NETN-BASE FOM Module provides common definitions of datatypes and extends the RPR-BASE FOM Module.

## Datatypes

### Simple Datatypes

|Name|Units|Semantics|
|---|---|---|
|AltitudeMeterFloat64|meters|The altitude in meters. The type of height is defined by the context of use (i.e. height Above Mean Sea Level, height Above Ground Level).|
|ConcentrationKgPerMeterCubedFloat32|Kg/m3|Concentration measured as Kg per cubic meter.|
|DegreesPerSecondFloat32|Degrees/second|The turn rate in degrees per second, where: (a) zero value: not turning; (b) positive value: turning right; (c) negative value: turning left.|
|DirectionDegreesFloat32|Degree of arc|Compass direction measured clockwise relative to an origin. If not stated elsewhere, the origin is true north. Value may be outside the interval [0, 360), and should then be interpreted as the corresponding value modulo 360 within the interval.|
|DraughtMeterFloat32|meters|The draught in meters.|
|EpochTimeSecInt64|Second|The number of seconds since 1 Jan 1970 (wallclock time) or since the start of the simulation (logical time).|
|IMOType|NA|The International Maritime Organization (IMO) number is a unique identifier for vessels.|
|LatLongDegreesFloat64|Degree of arc|Represents a measure of either latitude or longitude.|
|MIDType|NA|The Maritime Identification Digits (MID) for an individual vessel is a three digits code.|
|PercentFloat64|Percent (%)|A percentage (0-100).|
|QuantityFloat32|NA|A generic floating-point quantity.|
|QuantityFloat64|NA|A generic floating-point quantity.|
|QuantityInt32|NA|A generic discrete quantity.|
|ShipTypeType|NA|The type of ship and cargo.|
|TimeSecInt32|Second (s)|A time interval in seconds.|

### Enumerated Datatypes

|Name|Representation|Semantics|
|---|---|---|
|ActiveStatusEnum8|HLAoctet|An inactive object should not be shown on C4I systems and can not move or interact with other objects.|
|AggregateMissionEnum16|HLAinteger16BE|The specific value that represents the general class or nature of activity (from JC3IEDM action-event-category-code)|
|AltitudeTypeEnum8|HLAoctet|AMSL = Above Mean Sea Level, AGL = Abve Ground Level|
|AreaTypeEnum32|HLAinteger32BE|Specifies if the area is a polygon or a circle.|
|CancellationReasonEnum32|HLAinteger32BE|Describes the reason for the cancellation|
|DamageStatusEnhancedEnum32|HLAinteger32BE|The damage status of an object|
|EchelonEnum32|HLAinteger32BE|Identifies the unit's echelon level.|
|PathTypeEnum32|HLAinteger32BE|Specifies if the path is the actual path with waypoints or if it is a reference to registred NETN_GeoObject.Path through a UUID.|
|PointTypeEnum32|HLAinteger32BE|Specifies if the point is the actual location or if it is a reference to registred NETN_GeoObject.Point through a UUID.|

### Array Datatypes

|Name|Element|Cardinality|Semantics|
|---|---|---|---|
|ArrayOfStringType|HLAunicodeString|Dynamic|An general array datatype for representing a set of strings.|
|ArrayOfUuid|UuidArrayOfHLAbyte16|Dynamic|Array of Unique Identifiers expressed as UUIDs.|
|ArrayOfWorldLocationStruct|WorldLocationStruct|Dynamic|A polygonal chain with geocentric points, may be empty.|
|Callsign|HLAunicodeChar|Dynamic|Unique identifier for an entity. A more user friendly identifier than UUID, used in Logistics protocol for Consumer and Provider.|
|FederateName|HLAunicodeChar|Dynamic|HLA Federate Name|
|GeocentricPath|WorldLocationStruct|[2..2147483647]|An array of geocentric world locations with at least two elements.|
|GeocentricPolygon|WorldLocationStruct|[3..2147483647]|A polygon in world locations.|
|GeodeticPath|GeodeticLocation|[2..2147483647]|A list of lat, lon coordinates in WGS84 reference system specifying a path where each segement is a great circle between locations.|
|GeodeticPolygon|GeodeticLocation|[3..2147483647]|A geographical area bounded by a path where the first and last point in the path are closed. Each point is a geodetic coordinate in WGS84 on the earth surface. Each segment is a great circle between locations.|
|NETN_ArrayOfSupplyStruct|NETN_SupplyStruct|Dynamic|Array with NETN SupplyStructs|
|SymbolIdentifierArray15|HLAunicodeChar|15|MIL-STD-2525C symbol code.|
|SymbolIdentifierArray30|HLAunicodeChar|30|MIL-STD-2525D symbol code.|
|TransactionId|HLAbyte|16|Unique identifier for a transaction. Encoded according to RFC 4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs.|
|UUID|HLAbyte|16|4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs. For example, 00112233-4455-8877-6699-aabbccddeeff is encoded as the bytes 00 11 22 33 44 55 88 77 66 99 aa bb cc dd ee ff.|
|UuidArrayOfHLAbyte16|HLAbyte|16|UUIDs are exchanged as a byte array and are encoded according to RFC 4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs. For example, 00112233-4455-8877-6699-aabbccddeeff is encoded as the bytes 00 11 22 33 44 55 88 77 66 99 aa bb cc dd ee ff.|


### Fixed Record Datatypes

|Name|Fields|Semantics|
|---|---|---|
|GeocentricCircle|Location, Radius|Circle|
|GeodeticCircle|CenterPoint, Radius|A geodetic point and radius specifying a circle on the surface of the earth WGS84 where radius is a great circle distance on the surface.|
|GeodeticLocation|Latitude, Longitude|A geodetic point, specified by latitude and longitude, with unspecified altitude. WGS84|
|GeodeticQuadrangle|Point1, Point2|A latitude-longitude quadrangle is a region bounded by two meridians and two parallels.|
|NETN_SupplyStruct|SupplyType, Quantity|Same encoding as RPR2 SupplyStruct.|



### Variant Record Datatypes

|Name|Discriminant|Alternatives|Semantics|
|---|---|---|---|
|AreaVariantStruct|AreaTypeEnum32|Polygon, Circle|Defines the BaseStruct.|
|PathVariantStruct|PathTypeEnum32|Waypoints, UUID|Defines the path, either as a polygonal chain or a UUID that refers to a in the federation execution registred NETN_GeoObject.Path.|
|PointVariantStruct|PointTypeEnum32|Location, UUID|Defines the point, either a Location or a UUID reference to a NETN_GeoObject.Point.|


