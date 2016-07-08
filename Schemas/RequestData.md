
#AI.RequestData
Instance of Request represents completion of an external request to the application to do work, and contains a summary of that request execution and the results.
## ver: int
Schema version

Default value: 2

## id: string
Identifier of a request call instance. Used for correlation between request and other telemetry items.

**Question**: can we decrease limit to 64?

Max length: 1024

## duration: string
Request duration in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff.

## responseCode: string
Result of a request execution. Http status code for http requests.

**Question**: It is not sanitized in .NET SDK today. Make it be.

Max length: 1024

## success: bool
Indication of successfull or unsuccessfull call.

## source: string
Source of the request. Examples are instrumentation key of the caller, ip address of the caller.

Max length: 1024

This field is optional.

## name: string
Name of the request. Represents code path taken to process request. Low cardinality value to allow better grouping of requests. For http requests represents http method and url path template like 'GET /values/{id}'.

Max length: 1024

This field is optional.

## url: string
Request url with all query string parameters

**Question**: can we increase it to at least 8192?

Max length: 2048

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

