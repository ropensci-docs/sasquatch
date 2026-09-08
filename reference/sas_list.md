# List contents of a SAS directory

Lists the files or directories of a directory within the remote SAS
server.

## Usage

``` r
sas_list(path)
```

## Arguments

- path:

  string; Path of directory on remote SAS server to list the contents
  of.

## Value

`character` vector; File or directory names.

## See also

Other file management functions:
[`sas_file_copy()`](https://docs.ropensci.org/sasquatch/reference/sas_file_copy.md),
[`sas_file_download()`](https://docs.ropensci.org/sasquatch/reference/sas_file_download.md),
[`sas_file_exists()`](https://docs.ropensci.org/sasquatch/reference/sas_file_exists.md),
[`sas_file_remove()`](https://docs.ropensci.org/sasquatch/reference/sas_file_remove.md),
[`sas_file_upload()`](https://docs.ropensci.org/sasquatch/reference/sas_file_upload.md)

## Examples

``` r
if (FALSE) { # interactive()
sas_connect()

sas_list(".")
}
```
