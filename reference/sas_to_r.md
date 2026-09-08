# Convert SAS table to R

Converts table from current SAS session into a R `data.frame`.

## Usage

``` r
sas_to_r(table_name, libref = "WORK")
```

## Arguments

- table_name:

  string; Name of table in SAS.

- libref:

  string; Name of libref SAS table is stored within.

## Value

`data.frame` of the specified SAS table.

## Details

SAS only has two data types (numeric and character). Data types are
converted as follows:

- numeric -\> double

- character -\> character

- numeric (datetime, timezones are lost) -\> POSIXct

- numeric (date) -\> POSIXct

In the conversion process dates and datetimes are converted to local
time. If utilizing another timezone, use `attr(date, "tzone") <-` or
`lubridate::with_tz()` to convert back to the desired time zone.

## See also

[`sas_from_r()`](https://docs.ropensci.org/sasquatch/reference/sas_from_r.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect()

cars <- sas_to_r("cars", "sashelp")
}
```
