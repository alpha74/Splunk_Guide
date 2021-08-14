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




