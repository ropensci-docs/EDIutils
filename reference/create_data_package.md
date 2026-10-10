# Create data package

Create data package

## Usage

``` r
create_data_package(eml, env = "production")
```

## Arguments

- eml:

  (character) Full path to an EML file describing the data package to be
  created

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

transaction (character) Transaction identifier. May be used in a
subsequent call to
[`check_status_create()`](https://docs.ropensci.org/EDIutils/reference/check_status_create.md)
to determine the operation status

## Details

Each data entity described in `eml` must be accompanied by a web
accessible URL at the EML XPath ".//physical/distribution/online/url".
The EDI data repository downloads the data entities via this URL. The
URLs must be static and not have any redirects otherwise the data
entities will not be downloaded.

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Evaluation and Upload:
[`check_status_create()`](https://docs.ropensci.org/EDIutils/reference/check_status_create.md),
[`check_status_evaluate()`](https://docs.ropensci.org/EDIutils/reference/check_status_evaluate.md),
[`check_status_update()`](https://docs.ropensci.org/EDIutils/reference/check_status_update.md),
[`evaluate_data_package()`](https://docs.ropensci.org/EDIutils/reference/evaluate_data_package.md),
[`update_data_package()`](https://docs.ropensci.org/EDIutils/reference/update_data_package.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Create data package
transaction <- create_data_package(
  eml = paste0(tempdir(), "/edi.595.1.xml"),
  env = "staging"
)
transaction
#> [1] "create_163966765080210573__edi.595.1"

# Check creation status
status <- check_status_create(
  transaction = transaction,
  env = "staging"
)
status
#> [1] TRUE

logout()
} # }
```
