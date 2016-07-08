
#AI.MetricData
Instance of the Metric item is a list of measurements (single data points) and/or aggregations
## ver: int
Schema version

Default value: 2

## metrics: IList[DataPoint]
List of metrics.

[DataPoint] "Metric data single measurement."
    - name: string
    Name of the metric.
    
    Max length: 1024
    
    - kind: test.DataPointType
    Metric type.
    
    Default value: Measurement
    
    This field is optional.
    
    [DataPointType] "Type of the metric data measurement."
        - Measurement = 0
        - Aggregation = 1
        
    - value: double
    Metric calculated value.
    
    - count: int
    Metric weight of the aggregated metric. Should not be set for a measurement.
    
    This field is optional.
    
    - min: double
    Minimum value of the aggregated metric. Should not be set for a measurement.
    
    This field is optional.
    
    - max: double
    Maximum value of the aggregated metric. Should not be set for a measurement.
    
    This field is optional.
    
    - stdDev: double
    Standard deviation of the aggregated metric. Should not be set for a measurement.
    
    This field is optional.
    
    
## properties: IDictionary[string, string]
Collection of custom properties.

Max key length: 150

Max value length: 8192

This field is optional.

