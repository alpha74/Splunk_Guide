## Field and Fields Extraction



### Fields

- They are searchable key value pairs. 
- Eg: `user = user@xyz.com`


### Fields discovery

- Splunk automatically discovers fields.
- Default fields: `host, source, sourcetype`
- Splunk also looks for obvious key-value pairs in first 100 events.
- Splunk also does field extractions, which are stored in configuration files. 


### Fields Extraction
- Custom field extraction can be built using Splunk Field Extractor. 
- Use regular expressions to extract fields based on patterns.


### Field discovery Search modes

- Each of these has different performance.

- __Fast__
  - If seach contains transforming commands, eg: `timechart`, `stats`
  - This mode is good when we know all  fields that needs to be searched. 
  - Disables field discovery and hence search is faster.
 
- __Smart__
  - Default
  - Looks for key-value pairs.
  - Uses Field discovery


- __Verbose__
  - Should be used when we don't know much about about the data. 
  - Splunk uses full resources for fields auto discovery.
  - Slower search.

