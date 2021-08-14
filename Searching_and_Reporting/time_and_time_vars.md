# Time and Time Variables


### Time
- Splunk searches data from timestamps.
- Timestamps are converted to UNIX time and are stored in `_time` field and is used by `Time Range picker`.
- Splunk assumes that any data indexed is in the timezone of the Splunk instance. 
- In Splunk web, `_time` appears in human readable format, and can be manipulated in any format.
- Getting timestamp by splunk:
  - Looks for timestamps in the event data.
  - Source name or file name
  - File modification time
  - Current system time


#### Time Variables

- Useful when evaluating time and specifying time in SPL.

- __Time variables__
<img width="966" alt="image" src="https://user-images.githubusercontent.com/31771552/129445858-e543a225-fc2d-49aa-986a-3242c2874b6d.png">


- __Date variables__

<img width="958" alt="image" src="https://user-images.githubusercontent.com/31771552/129445887-22a8f9a5-8558-4eea-95c0-d8955199cb6a.png">


