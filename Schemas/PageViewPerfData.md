
#AI.PageViewPerfData
Instance of PageView represents: page view with no performance data, page view with performance data, just the performance data of an earlier page request
## ver: int
Schema version

Default value: 2

## name: string
Event name. Keep it low cardinality to allow proper grouping and useful metrics.

**Question**: Why Custom Event name is shorter than Request name or dependency name?

Max length: 512

## properties: IDictionary[string, string]
Collection of custom properties.

Max key length: 150

Max value length: 8192

This field is optional.

## measurements: IDictionary[string, double]
Collection of custom measurements.

Max key length: 150

This field is optional.

## url: string
Request url with all query string parameters

**Question**: can we increase it to at least 8192?

Max length: 2048

This field is optional.

## duration: string
Request duration in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff. For a page view (PageViewData), this is the duration. For a page view with performance information (PageViewPerfData), this is the page load time.

This field is optional.

## referrer: string
Referrer url. Never used so far.

**Question**: Should we deprecated it or make official?

Max length: 1024

This field is optional.

## referrerData: string
???

**Question**: What is this field for?

Max length: 8192

This field is optional.

## perfTotal: string
Performance total in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff

This field is optional.

## networkConnect: string
Network connection time in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff

This field is optional.

## sentRequest: string
Sent request time in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff

This field is optional.

## receivedResponse: string
Received response time in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff

This field is optional.

## domProcessing: string
DOM processing time in TimeSpan 'G' (general long) format: d:hh:mm:ss.fffffff

This field is optional.

