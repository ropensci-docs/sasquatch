# Execute SAS code string

Execute SAS code in current session and render html output.

## Usage

``` r
sas_run_string(input, capture = "both", height = "auto", width = "auto")
```

## Arguments

- input:

  string; SAS code to run.

- capture:

  string; If `"both"`, tabpanel with output and log included. If
  `"listing"`, only output is included. If `"log"` only log is included.

- height:

  string; The height of the SAS output.

- width:

  string; The width of the SAS output.

## Value

`htmlwidget`; HTML5 output.

## See also

Other code execution functions:
[`sas_run_file()`](https://docs.ropensci.org/sasquatch/reference/sas_run_file.md),
[`sas_run_selected()`](https://docs.ropensci.org/sasquatch/reference/sas_run_selected.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect()

sas_run_string("PROC MEANS DATA = sashelp.cars;RUN;")
}
```
