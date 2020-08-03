# NETN-BASE
NATO Education and Training Network (NETN) Base Datatypes (BASE) Module. 
        
This module is a base module for all other NETN-FOM modules. It specifies standard data types and structures and extends the RPR-BASE module. The specification is based on IEEE 1516 High Level Architecture (HLA) Object Model Template (OMT) and primarily intended to support interoperability in a federated simulation (federation) based on HLA. An HLA OMT based Federation Object Model (FOM) is used to specify types of data and its encoding on the network. The NETN-BASE FOM module is available as an XML file for use in HLA based federations.
        
## Purpose
The NETN-BASE FOM Module provides standard definitions of datatypes and extends the RPR-BASE FOM Module.

## Datatypes

### Simple Datatypes

|Name|Units|Semantics|
|---|---|---|
|AltitudeMeterFloat64|Meter|Generic representation of altitude defined by the context of use, i.e. height Above Mean Sea Level, height Above Ground Level.|
|DegreesPerSecondFloat32|Degrees/second|The turn rate in degrees per second, where: (a) zero value: not turning; (b) positive value: turning right; (c) negative value: turning left.|
|DirectionDegreesFloat32|Degree|Compass direction measured clockwise relative to true north. Calculate values outside the range [0, 360) as modulo 360.|
|DraughtMeterFloat32|Meter|The vertical distance between the waterline and the bottom of the hull (keel), with the thickness of the hull included; Draught determines the minimum depth of water a ship or boat can safely navigate.|
|EpochTimeSecInt64|Second|The number of seconds since 1 Jan 1970 (wallclock time) or since the start of the simulation (logical time).|
|IMOType|NA|The International Maritime Organization (IMO) number is a unique identifier for vessels.|
|LatLongDegreesFloat64|Degree|Represents a measure of either latitude or longitude in decimal degrees of arc.|
|MassConcentrationFloat32|kg/m3|Concentration of a substance measured as kg per cubic meter.|
|MassDensityFloat32|kg/m3|Density of a substance measured as kg per cubic meter.|
|MIDType|NA|The Maritime Identification Digits (MID) for an individual vessel is a three digits code.|
|PercentFloat64|Percent|A generic measure of percentage (0-100).|
|QuantityFloat32|NA|A generic floating-point quantity.|
|QuantityFloat64|NA|A generic floating-point quantity.|
|QuantityInt32|NA|A generic discrete quantity.|
|ShipTypeType|NA|The type of ship and cargo.|
|TimeSecInt32|Second|A generic time interval in seconds.|

### Enumerated Datatypes

|Name|Representation|Semantics|
|---|---|---|
|ActiveStatusEnum8|HLAoctet|A state which indicates the status of an object concerning its participation in the simulation. An object in an inactive state is not simulated and does not interact with other objects.|
|AggregateMissionEnum16|HLAinteger16BE|Representation of the general class or nature of activity related to a unit's mission. Enumerations are based on JC3IEDM action-event-category-code.|
|AltitudeTypeEnum8|HLAoctet|The reference for altitude. AMSL = Above Mean Sea Level or AGL = Abve Ground Level.|
|AreaTypeEnum32|HLAinteger32BE|Specifies if a generic area is a polygon or a circle.|
|CancellationReasonEnum32|HLAinteger32BE|Describes the reason for a cancellation.|
|DamageStatusEnhancedEnum32|HLAinteger32BE|The damage status of an object.|
|EchelonEnum32|HLAinteger32BE|The echelon level of a unit.|
|PathTypeEnum32|HLAinteger32BE|Specifies if a path is defined by waypoints or by reference to a path object in the federation.|
|PointTypeEnum32|HLAinteger32BE|Specifies if a point is defined by a location or by reference to a point object in the federation.|

### Array Datatypes

|Name|Element|Cardinality|Semantics|
|---|---|---|---|
|ArrayOfStringType|HLAunicodeString|Dynamic|A generic representation of a set of strings.|
|ArrayOfUuid|UuidArrayOfHLAbyte16|Dynamic|Deprecated. Array of Unique Identifiers expressed as UUIDs.|
|ArrayOfUUID|UUID|Dynamic|A set of Unique Identifiers as UUID.|
|ArrayOfWorldLocationStruct|WorldLocationStruct|Dynamic|A polygonal chain (path) expressed as a sequence of geocentric points.|
|Callsign|HLAunicodeChar|Dynamic|Identifier for a simulated entity. Callsigns should be unique in the context in which they are used but are not required to be globally unique.|
|FederateName|HLAunicodeChar|Dynamic|The unique name of a federate participating in an HLA federation.|
|GeocentricPath|WorldLocationStruct|[2..2147483647]|An array of geocentric world locations with at least two elements.|
|GeocentricPolygon|WorldLocationStruct|[3..2147483647]|A polygon defined as a closed polygonal chain of geocentric world locations where the last location is connected to the first.|
|GeodeticPath|GeodeticLocation|[2..2147483647]|A sequence of geodetic locations defining a path where each segment is a great circle between locations.|
|GeodeticPolygon|GeodeticLocation|[3..2147483647]|A sequence of geodetic locations defining a geographical area bounded by a closed path where the first and last locations in the sequence are connected. Each point is a geodetic coordinate in WGS84 on the earth surface, and each segment is a great circle between locations.|
|NETN_ArrayOfSupplyStruct|NETN_SupplyStruct|Dynamic|A set of supply descriptions.|
|SymbolIdentifierArray15|HLAunicodeChar|15|MIL-STD-2525C symbol code.|
|SymbolIdentifierArray30|HLAunicodeChar|30|MIL-STD-2525D symbol code.|
|TransactionId|HLAbyte|16|Unique identifier for a transaction. Encoded according to RFC 4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs.|
|UUID|HLAbyte|16|4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs. For example, 00112233-4455-8877-6699-aabbccddeeff is encoded as the bytes 00 11 22 33 44 55 88 77 66 99 aa bb cc dd ee ff.|
|UuidArrayOfHLAbyte16|HLAbyte|16|Deprecated. UUIDs are exchanged as a byte array and are encoded according to RFC 4122, section 4.1.2 using 16 bytes. Also referred to as Variant 1 or RFC 4122/DCE 1.1 UUIDs. For example, 00112233-4455-8877-6699-aabbccddeeff is encoded as the bytes 00 11 22 33 44 55 88 77 66 99 aa bb cc dd ee ff.|

### Fixed Record Datatypes

|Name|Fields|Semantics|
|---|---|---|
|GeocentricCircle|Location, Radius|A circle on the local tangent plane (North-East-Down) of the centre at the specified location.|
|GeodeticCircle|CenterPoint, Radius|A geodetic point and radius specifying a circle on the surface of the earth WGS84 where the radius is a great circle distance on the surface.|
|GeodeticLocation|Latitude, Longitude|A geodetic point, specified by latitude and longitude, with unspecified altitude. WGS84|
|GeodeticQuadrangle|Point1, Point2|A latitude-longitude quadrangle is a region bounded by two meridians and two parallels.|
|NETN_SupplyStruct|SupplyType, Quantity|Description of supply. Same encoding as RPR2 SupplyStruct.|

### Variant Record Datatypes

|Name|Discriminant|Alternatives|Semantics|
|---|---|---|---|
|AreaVariantStruct|AreaTypeEnum32|Polygon, Circle|Description of an area in the local tangent plane (North-East-Down) of the alternatives.|
|PathVariantStruct|PathTypeEnum32|Waypoints, UUID|Defines a path, either as a polygonal chain of waypoints or a UUID that refers to a path object in the federation.|
|PointVariantStruct|PointTypeEnum32|Location, UUID|Defines the point, either a Location or a UUID reference to a point object in the federation.|


