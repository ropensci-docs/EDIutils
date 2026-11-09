# Update data package

Update data package

## Usage

``` r
update_data_package(eml, useChecksum = FALSE, env = "production")
```

## Arguments

- eml:

  (character) Full path to an EML file describing the data package to be
  updated

- useChecksum:

  (logical) Use data entities from a previous version of the data
  package? See details below.

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

transaction (character) Transaction identifier. May be used in a
subsequent call to
[`check_status_update()`](https://docs.ropensci.org/EDIutils/reference/check_status_update.md)
to determine the operation status

## Details

Each data entity described in `eml` must be accompanied by a web
accessible URL at the XPath ".//physical/distribution/online/url". The
EDI data repository uses these links to download the data entities. The
URLs must be static and not have any redirects otherwise the data
entities will not be downloadable.

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Evaluation and Upload:
[`check_status_create()`](https://docs.ropensci.org/EDIutils/reference/check_status_create.md),
[`check_status_evaluate()`](https://docs.ropensci.org/EDIutils/reference/check_status_evaluate.md),
[`check_status_update()`](https://docs.ropensci.org/EDIutils/reference/check_status_update.md),
[`create_data_package()`](https://docs.ropensci.org/EDIutils/reference/create_data_package.md),
[`evaluate_data_package()`](https://docs.ropensci.org/EDIutils/reference/evaluate_data_package.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Update data package
transaction <- update_data_package(
  eml = paste0(tempdir(), "/edi.595.2.xml"),
  env = "staging"
)
transaction
#> [1] "update_edi.595_163966788658131920__edi.595.2"

# Check update status
status <- check_status_update(
  transaction = transaction,
  env = "staging"
)
status
#> [1] TRUE

logout()
} # }
```
