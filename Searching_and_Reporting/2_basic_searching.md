## Basic Searching


### Broad search terms in metadata:

- __Index__
  - `index=main` , `index=notif*`

- __Host__
  - `host=server.com` , `host=dashboard-*`

- __Source or SourceType__
  - `source=/var/lib` , `source=nb.log`

-----

- __Keywords__
  - `failed`, `error`, `exception`

- __Phrases__
  - `"error occured"` , `"for account:"`

- __Fields__
  - Key-value pairs
  - `user=user.xyz.com`


-----

- __Wildcards__
   - `failed*`, `error*`


- __Booleans__
  - Spaces indicate boolean AND.
  - `AND` , `OR`, `NOT`


-----

### Basic search commands

- `chart` or `timechart`
  - Returns results in tabular output for charting.

- `rename`
  - Rename a specific field.

- `sort`
  - Sorts results by specified field.
  - `sort -FIELD_NAME` will sort in descending order.

- `stats`
  -  Builds statistics table.

- `eval`
  - Calculates an expression. 

- `dedup`
   - Removes duplicates.


- `Table`
  - Builds table with specific fields.


-----


#### Sample commands


__Search query__ : `index=notif* "MemoryUtils"`

- __Events__

```
[2021-08-15 14:22:30.963] [MemoryUtils stats] [INFO] c.w.u.MemoryUtils max = 8038m, free = 6036m
[2021-08-15 14:22:30.905] [MemoryUtils stats] [INFO] c.w.u.MemoryUtils max = 8038m, free = 3182m
[2021-08-15 14:22:30.679] [MemoryUtils stats] [INFO] c.w.u.MemoryUtils max = 8038m, free = 3722m
```

- __Table__

  - `index=notif* "MemoryUtils" | table _time max free | sort -_time`

<img width="1227" alt="image" src="https://user-images.githubusercontent.com/31771552/129472884-bbed66bb-3f0a-4de7-b95e-442e0faca5c8.png">


