# Check SAS session

Checks if a SAS session currently exists. If the SAS session has
terminated during the session, `check_session()` will not detect it.

## Usage

``` r
check_session(call = rlang::caller_env())
```

## Details

Use
[`execute_if_connection_active()`](https://docs.ropensci.org/sasquatch/reference/execute_if_connection_active.md)
for any function that relies on a SAS connection to catch inactive
sessions.
