
#Microsoft.Telemetry.Envelope
System variables for a telemetry item (Part A)
## ver: int
Default value: 1

This field is optional.

## name: string
Type name of telemetry data item.

Max length: 1024

## time: string
The UTC time the telemetry item was created. ISO 8601 zero offset date-time string. Example: 2009-06-15T13:45:30.0000000Z

## sampleRate: double
Sampling rate used in application. This telemetry item represents 1 / sampleRate actual telemetry item.

**Question**: Do we use this sampleRate or one in ContextTagKeys collection?

Default value: 100.0

This field is optional.

## seq: string
Sequence field used to track absolute order of uploaded events.

Max length: 64

This field is optional.

## iKey: string
The application's instrumentation key.

Max length: 40

This field is optional.

## tags: IDictionary[string, string]
Key/value collection of context properties. See ContextTagKeys for information on available properties.

This field is optional.

## data: Base
Telemetry data item.

This field is optional.

