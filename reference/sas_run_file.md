# Execute SAS file

Execute a SAS file and render html output or save output as html and
log.

## Usage

``` r
sas_run_file(input_path, output_path, overwrite = FALSE)
```

## Arguments

- input_path:

  string; Path of SAS file to run.

- output_path:

  optional string; Path to save html output to (log file will be named
  the same).

- overwrite:

  logical; Can output overwrite prior output?

## Value

If `output_path` specified, `htmlwidget`. Else, no return value.

## See also

Other code execution functions:
[`sas_run_selected()`](https://docs.ropensci.org/sasquatch/reference/sas_run_selected.md),
[`sas_run_string()`](https://docs.ropensci.org/sasquatch/reference/sas_run_string.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect()

tempfile_sas_path <- tempfile(fileext = ".sas")
tempfile_html_path <- sub("\\.sas$", ".html", tempfile_sas_path)
tempfile_log_path <- sub("\\.sas$", ".log", tempfile_sas_path)
cat("PROC MEANS DATA = sashelp.cars;RUN;", file = tempfile_sas_path)
sas_run_file(tempfile_sas_path, tempfile_html_path)

# clean up
unlink(tempfile_sas_path)
unlink(tempfile_html_path)
unlink(tempfile_log_path)
}
```
