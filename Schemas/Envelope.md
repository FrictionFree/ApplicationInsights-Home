
#Microsoft.Telemetry.Envelope
System variables for a telemetry item.

1. **ver** : int

    Envelope version. For internal use only. By assigning this the default, it will not be serialized within the payload unless changed to a value other than #1.
    
    Default value: 1
    
    This field is optional.
    
1. **name** : string

    Type name of telemetry data item.
    
    Max length: 1024
    
1. **time** : string

    The UTC time the telemetry item was created. ISO 8601 zero offset date-time string. Example: 2009-06-15T13:45:30.0000000Z
    
    Time offset in the past from the current time: -48 hours
    
    Time offset in the future from the current time: +2 hours
    
1. **sampleRate** : double

    Sampling rate used in application. This telemetry item represents 1 / sampleRate actual telemetry item.
    
    Default value: 100.0
    
    This field is optional.
    
1. **seq** : string

    Sequence field used to track absolute order of uploaded events.
    
    Max length: 64
    
    This field is optional.
    
1. **iKey** : string

    The application's instrumentation key.
    
    Max length: 40
    
    This field is optional.
    
1. **tags** : IDictionary[string, string]

    Key/value collection of context properties. See ContextTagKeys for information on available properties.
    
    This field is optional.
    
1. **data** : Base

    Telemetry data item.
    
    This field is optional.
    
