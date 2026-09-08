# Get current SAS session

Returns the current SAS session, which can be used to extend `sasquatch`
functionality or access the current session within Python.

## Usage

``` r
sas_get_session()
```

## Value

`saspy.sasbase.SASsession`; Current SAS session.

## Details

### Extending `sasquatch` functionality

`SASPy` has a wealth of functionality, some of which have not all been
implemented within `sasquatch`. `sas_get_session()` offers a gateway to
unimplemented functionality within the [SASsession
class](https://sassoftware.github.io/saspy/api.html#sas-session-object).

### Using Python

When utilizing Python, R, and SAS, start the session within R using
[`sas_connect()`](https://docs.ropensci.org/sasquatch/reference/sas_connect.md)
and utilize `reticulate` to pass the `saspy.sasbase.SASsession` object
to Python.

## See also

Other session management functions:
[`sas_connect()`](https://docs.ropensci.org/sasquatch/reference/sas_connect.md),
[`sas_disconnect()`](https://docs.ropensci.org/sasquatch/reference/sas_disconnect.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect()

sas_get_session()
}
```
