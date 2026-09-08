# Execute selected SAS code

Execute selected SAS code in current session and render html output as
SAS widget. See
[`vignette("overview")`](https://docs.ropensci.org/sasquatch/articles/overview.md)
for more information on how to utilize the addin within RStudio or
Positron.

## Usage

``` r
sas_run_selected()
```

## Value

`htmlwidget`; HTML5 output.

## See also

Other code execution functions:
[`sas_run_file()`](https://docs.ropensci.org/sasquatch/reference/sas_run_file.md),
[`sas_run_string()`](https://docs.ropensci.org/sasquatch/reference/sas_run_string.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect()

# highlight something in the active editor of RStudio or Positron

sas_run_selected()
}
```
