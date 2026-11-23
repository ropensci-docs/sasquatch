# Install SASPy package

Installs the `SASPy` package and its dependencies within a virtual
Python environment.

Behavior was derived from `tensorflow::install_tensorflow()`.

## Usage

``` r
install_saspy(
  method = c("auto", "virtualenv", "conda"),
  conda = "auto",
  envname = "r-saspy",
  extra_packages = NULL,
  restart_session = TRUE,
  conda_python_version = NULL,
  ...,
  pip_ignore_installed = FALSE,
  new_env = identical(envname, "r-saspy"),
  python_version = NULL
)
```

## Arguments

- method:

  By default, `“auto”` automatically finds a method that will work in
  the local environment. Change the default to force a specific
  installation method.

- conda:

  The path to a conda executable. Use `"auto"` to allow reticulate to
  automatically find an appropriate conda binary.

- envname:

  The name, or full path, of the environment in which Python packages
  are to be installed.

- extra_packages:

  Additional packages to install.

- restart_session:

  Restart session?

- conda_python_version:

  Passed to conda (only applicable if `method = "conda"`)

- ...:

  other arguments passed to
  [`reticulate::conda_install()`](https://rstudio.github.io/reticulate/reference/conda-tools.html)
  or
  [`reticulate::virtualenv_install()`](https://rstudio.github.io/reticulate/reference/virtualenv-tools.html),
  depending on the `method` used.

- pip_ignore_installed:

  Should pip ignore installed python packages and reinstall all already
  installed python packages?

- new_env:

  If `TRUE`, any existing Python virtual environment and/or conda
  environment specified by `envname` is deleted first.

- python_version:

  Select the Python that will be used to create the virtualenv. Pass a
  string with version constraints like `"3.8"`, or `">=3.9,<=3.11"` or a
  file path to a `python` executable like `"/path/to/bin/python3"`. The
  supplied value is passed on to
  [`reticulate::virtualenv_starter()`](https://rstudio.github.io/reticulate/reference/virtualenv-tools.html).
  Note that `SASPy` requires a Python version of at least \>=3.4.

## Value

No return value.

## See also

[`configure_saspy()`](https://docs.ropensci.org/sasquatch/reference/configure_saspy.md)

## Examples

``` r
if (FALSE) { # interactive()
install_saspy(
  envname = "new-sasquatch-env",
  extra_packages = c("matplotlib", "numpy"),
)
}
```
