# Configure SASPy package

Adds `sascfg_personal.py` and `authinfo` files and prefills relevant
info according to a specified template.

## Usage

``` r
configure_saspy(template = c("none", "oda"), overwrite = FALSE)
```

## Arguments

- template:

  Default template to base configuration files off of.

- overwrite:

  Can new configuration files overwrite existing config files (if they
  exist)?

## Value

No return value.

## Details

Configuration for SAS can vary greatly based on your computer's
operating system and the SAS platform you wish to connect to (see
[`vignette("configuration")`](https://docs.ropensci.org/sasquatch/articles/configuration.md)
for more information).

Regardless of your desired configuration, configuration always starts
with the creation of a `sascfg_personal.py` file within the `SASPy`
package installation. This will look like:

    SAS_config_names = ['config_name']

    config_name = {

    }

`SAS_config_names` should contain a string list of the variable names of
all configurations. Configurations are specified as dictionaries, and
configuration parameters depend on the access method.

Additionally, some access methods will require an additional
authentication file (`.authinfo` for Linux and Mac, `_authinfo` for
Windows) stored in the user's home directory, which are constructed as
follows:

    config_name user {your username} password {your password}

### Templates

The `"none"` template simply creates a `sascfg_personal.py` file within
the `SASPy` package installation.

The `"oda"` template will set up a configuration for SAS On Demand for
Academics. The `sascfg_personal.py` and `authinfo` files will be
automatically configured using the information you provide through
prompts.

## See also

[`install_saspy()`](https://docs.ropensci.org/sasquatch/reference/install_saspy.md)

## Examples

``` r
if (FALSE) { # interactive()

# set up an ODA connection
config_saspy(template = "oda")
}
```
