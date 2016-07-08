
#Microsoft.Telemetry.Envelope
System variables for a telemetry item (Part A)
1. **ver** : int

    Default value: 1
    
    This field is optional.
    
1. **name** : string

    Type name of telemetry data item.
    
    Max length: 1024
    
1. **time** : string

    The UTC time the telemetry item was created. ISO 8601 zero offset date-time string. Example: 2009-06-15T13:45:30.0000000Z
    
1. **sampleRate** : double

    Sampling rate used in application. This telemetry item represents 1 / sampleRate actual telemetry item.
    
    **Question**: Do we use this sampleRate or one in ContextTagKeys collection?
    
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
    
