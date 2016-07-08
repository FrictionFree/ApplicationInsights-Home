
#AI.AvailabilityData
1. **ver** : int

    Schema version
    
    Default value: 2
    
1. **testRunId** : string

    **Question**: This is a new limit. Verify it's ok
    
    Max length: 64
    
1. **testTimeStamp** : string

1. **testName** : string

    **Question**: This is a new limit. Verify it's ok
    
    Max length: 1024
    
1. **duration** : string

    Duration in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff
    
1. **result** : test.TestResult

    [TestResult] "Instances of AvailabilityData represent the result of executing an availability test"
    
        - Pass = 0
        - Fail = 1
        
1. **runLocation** : string

    **Question**: This is a new limit. Verify it's ok
    
    Max length: 1024
    
    This field is optional.
    
1. **message** : string

    **Question**: This is a new limit. Verify it's ok
    
    Max length: 8192
    
    This field is optional.
    
1. **dataSize** : double

    This field is optional.
    
1. **properties** : IDictionary[string, string]

    Collection of custom properties.
    
    Max key length: 150
    
    Max value length: 8192
    
    This field is optional.
    
1. **measurements** : IDictionary[string, double]

    Collection of custom measurements.
    
    Max key length: 150
    
    This field is optional.
    
