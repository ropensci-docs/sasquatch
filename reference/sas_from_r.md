# Convert R table to SAS

Converts R table into a table in the current SAS session. R tables must
only have logical, integer, double, factor, character, POSIXct, or Date
class columns.

## Usage

``` r
sas_from_r(x, table_name, libref = "WORK", factors_as_strings = TRUE)
```

## Arguments

- x:

  `data.frame`; R table.

- table_name:

  string; Name of table to be created in SAS.

- libref:

  string; Name of libref to store SAS table within.

- factors_as_strings:

  logical; If `TRUE`, factors will become SAS strings. Else, factors
  will become formatted numerics.

## Value

`data.frame`; `x`.

## Details

SAS only has two data types (numeric and character). Data types are
converted as follows:

- logical -\> numeric

- integer -\> numeric

- double -\> numeric

- factor -\> character

- character -\> character

- POSIXct -\> numeric (datetime; timezones are lost)

- Date -\> numeric (date)

## See also

[`sas_to_r()`](https://docs.ropensci.org/sasquatch/reference/sas_to_r.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect()

sas_from_r(mtcars, "mtcars")
}
```
