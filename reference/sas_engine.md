# A SAS engine for `knitr`

Produces HTML or latex output for rending within quarto or rmarkdown
documents.

## Usage

``` r
sas_engine(options)
```

## Arguments

- options:

  Options from `knitr`.

## Value

`knitr` engine output.

## Details

Will be activated by running
[`library(sasquatch)`](https://docs.ropensci.org/sasquatch/)

### Supported `knitr` chunk options

`sasquatch`'s engine implements may of the same options as the R engine
in `knitr`, but not all.

- `eval` (Default: `TRUE`): Evaluate the code chunk (if false, just
  echos the code into the output)

- `echo` (Default: `TRUE`): Include the source code in output

- `output` (Default: `TRUE`): Include the results of executing the code
  in the output (`TRUE` or `FALSE`).

- `include` (Default: `TRUE`): Include any output (code or results).

- `capture` (Only within HTML; Default: `"both"`): If `"both"`, tabpanel
  with output and log included. If `"listing"`, only output is included.
  If `"log"` only log is included.

- `out.width` (Only within HTML; Default: `"auto"`): Width of output.

- `out.height` (Only within HTML; Default: `"auto"`): Height of output.

## Examples

``` r
# The below function is run internally within `sasquatch` on startup
knitr::knit_engines$set(sas = sas_engine)
```
