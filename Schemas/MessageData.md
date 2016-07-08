
#AI.MessageData
Instances of Message represent printf-like trace statements that are text-searched. Log4Net, NLog and other text-based log file entries are be translated into intances of this type. The message does not have measurements, and there is an ongoing debate if messages can have custom propertis
## ver: int
Schema version

Default value: 2

## message: string
Trace message

Max length: 32768

## severityLevel: test.SeverityLevel
Trace severity level.

This field is optional.

[SeverityLevel] "Defines the level of severity for the event."
    - Verbose = 0
    - Information = 1
    - Warning = 2
    - Error = 3
    - Critical = 4
    
## properties: IDictionary[string, string]
Collection of custom properties.

Max key length: 150

Max value length: 8192

This field is optional.

