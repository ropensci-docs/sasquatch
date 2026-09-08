# Delete a file or directory from SAS

Deletes a file or directory from the remote SAS server. Is analogous to
[`file.remove()`](https://rdrr.io/r/base/files.html), but for the remote
SAS server.

## Usage

``` r
sas_file_remove(path)
```

## Arguments

- path:

  string; Path of file on remote SAS server to be deleted.

## Value

`logical`; value indicating if the operation succeeded.

## See also

Other file management functions:
[`sas_file_copy()`](https://docs.ropensci.org/sasquatch/reference/sas_file_copy.md),
[`sas_file_download()`](https://docs.ropensci.org/sasquatch/reference/sas_file_download.md),
[`sas_file_exists()`](https://docs.ropensci.org/sasquatch/reference/sas_file_exists.md),
[`sas_file_upload()`](https://docs.ropensci.org/sasquatch/reference/sas_file_upload.md),
[`sas_list()`](https://docs.ropensci.org/sasquatch/reference/sas_list.md)

## Examples

``` r
if (FALSE) { # interactive()
# connect to SAS
sas_connect()

# create an example file
local_path <- tempfile(fileext = ".txt")
cat("some example text", file = tempfile_path)

sas_path <- readline(
  "Please provide the full path to upload an example file to (e.g., ~/example.txt)."
)
sas_file_upload(local_path, sas_path)

sas_file_remove(sas_path)

# cleanup
unlink(local_path)
}
```
