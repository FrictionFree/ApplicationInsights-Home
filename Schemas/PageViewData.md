
#AI.PageViewData
Instance of PageView represents a generic action on a page like a button click. It is also the base type for PageView.
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

