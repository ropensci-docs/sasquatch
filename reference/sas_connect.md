# Establish SAS session

Starts a SAS session. This is required before doing anything!

## Usage

``` r
sas_connect(cfgname, reconnect = FALSE)
```

## Arguments

- cfgname:

  string; Name of configuration to use from the SAS_config_names list
  within in `sascfg_personal.py`.

- reconnect:

  logical; Establish a new connection if a connection already exists?

## Value

No return value.

## Details

All configurations are specified within the `sascfg_personal.py` file
inside the `SASPy` package. For more information about `SASPy`
configuration, check out the [configuration
documentation](https://sassoftware.github.io/saspy/configuration.html)
or
[`vignette("configuration")`](https://docs.ropensci.org/sasquatch/articles/configuration.md).

## See also

Other session management functions:
[`sas_disconnect()`](https://docs.ropensci.org/sasquatch/reference/sas_disconnect.md),
[`sas_get_session()`](https://docs.ropensci.org/sasquatch/reference/sas_get_session.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect(cfgname = "oda")
}
```
