# Execute SASPy function if session is active

Executes the code passed to it if the connection is active and provides
a more helpful error message if no connection is active.

## Usage

``` r
execute_if_connection_active(code, call = rlang::caller_env())
```

## Details

The SAS connection is asynchronous so it can become inactive without the
user knowing. When the connection is inactive and an action is preformed
it will check the connection and raise an error.
