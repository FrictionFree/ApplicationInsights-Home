
#AI.AvailabilityData
## ver: int
Schema version

Default value: 2

## testRunId: string
**Question**: This is a new limit. Verify it's ok

Max length: 64

## testTimeStamp: string
## testName: string
**Question**: This is a new limit. Verify it's ok

Max length: 1024

## duration: string
Duration in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff

## result: test.TestResult
[TestResult] "Instances of AvailabilityData represent the result of executing an availability test"
    - Pass = 0
    - Fail = 1
    
## runLocation: string
**Question**: This is a new limit. Verify it's ok

Max length: 1024

This field is optional.

## message: string
**Question**: This is a new limit. Verify it's ok

Max length: 8192

This field is optional.

## dataSize: double
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

