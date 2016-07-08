
#AI.RemoteDependencyData
Instance of Remote Dependency represents an interaction of the monitored component with a remote component/service like SQL or http endpoint.
## ver: int
Schema version

Default value: 2

## name: string
Name of the command initiated with this dependency call. Low cardinality value. Example are stored procedure name, url path template.

Max length: 1024

## id: string
Identifier of a dependency call instance. Used for correlation with the request telemetry item corresponding to this dependency call.

**Question**: can we decrease limit to 64?

Max length: 1024

This field is optional.

## resultCode: string
Result code of a dependency call. Examples are SQL error code, http status code.

**Question**: can we decrease limit to 1024?

Max length: 8192

This field is optional.

## value: double
Duration of a call in milliseconds.

**Question**: Should we change it to timespan as everything else?

## success: bool
Indication of successfull or unsuccessfull call.

Default value: true

This field is optional.

## commandName: string
Command initiated by this dependency call. Examples are SQL statement, http url with all query parameters.

**Question**: can we increase it to at least 8192?

Max length: 2048

This field is optional.

## dependencyTypeName: string
Dependency type name. Very low cardinality value for logical grouping of dependencies and interpretation of other fields like commandName and resultCode. Examples are SQL, Azure table, HTTP.

Max length: 1024

This field is optional.

## target: string
Target site of a dependency call. Examples are server name, host address.

Max length: 1024

This field is optional.

## properties: IDictionary[string, string]
Collection of custom properties.

Max key length: 150

Max value length: 8192

This field is optional.

## measurements: IDictionary[string, double]
Collection of custom measurements.

Max key length: 150

This field is optional.

