# Changelog

## sasquatch (development version)

## sasquatch 0.1.3

CRAN release: 2026-02-27

- Tabsets no longer alter each other’s states.
- Tabsets properly render in the ropensci docs.

## sasquatch 0.1.1

## sasquatch 0.1.0

### Features

- Added `out.height` and `out.width` arguments to HTML engine. HTML
  engine now returns an htmlwidget
  ([\#13](https://github.com/ropensci/sasquatch/issues/13))
- Added `capture`, `height`, `width` to
  [`sas_run_string()`](https://docs.ropensci.org/sasquatch/reference/sas_run_string.md).
  ([\#13](https://github.com/ropensci/sasquatch/issues/13))

### rOpenSci Review Changes

- [`configure_saspy()`](https://docs.ropensci.org/sasquatch/reference/configure_saspy.md)
  no longer asks that users type in their SAS ODA username and password
  within the terminal. See
  [`vignette("secrets", "httr")`](https://httr.r-lib.org/articles/secrets.html).  
- Dataset used to show
  [`sas_to_r()`](https://docs.ropensci.org/sasquatch/reference/sas_to_r.md)
  in `README.md` changed to `warpbreaks` and the variable name of the
  version of `"sashelp.cars"` was renamed to `sas_cars`.
- Fixed typo in
  [`configure_saspy()`](https://docs.ropensci.org/sasquatch/reference/configure_saspy.md).
  Changed Europe 2 to Europe 1.  
- Specified `rlang` imports.  
- Added a Code of Conduct.  
- A more informative error is now shown when a `reticulate::use_*`
  function is used for an environment without `SASPy` installed.
  ([\#11](https://github.com/ropensci/sasquatch/issues/11))
- [`install_saspy()`](https://docs.ropensci.org/sasquatch/reference/install_saspy.md)
  now supports conda environments.
  ([\#11](https://github.com/ropensci/sasquatch/issues/11))
