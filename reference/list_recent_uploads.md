# List recent uploads

List recent uploads

## Usage

``` r
list_recent_uploads(type, limit = 5, as = "data.frame", env = "production")
```

## Arguments

- type:

  (character) Upload type. Can be: "insert" or "update".

- limit:

  (numeric) Maximum number of results to return

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) Data package uploads

## See also

Other Listing:
[`list_data_descendants()`](https://docs.ropensci.org/EDIutils/reference/list_data_descendants.md),
[`list_data_entities()`](https://docs.ropensci.org/EDIutils/reference/list_data_entities.md),
[`list_data_package_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_identifiers.md),
[`list_data_package_revisions()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_revisions.md),
[`list_data_package_scopes()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_scopes.md),
[`list_data_sources()`](https://docs.ropensci.org/EDIutils/reference/list_data_sources.md),
[`list_deleted_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_deleted_data_packages.md),
[`list_recent_changes()`](https://docs.ropensci.org/EDIutils/reference/list_recent_changes.md),
[`list_service_methods()`](https://docs.ropensci.org/EDIutils/reference/list_service_methods.md),
[`list_user_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_user_data_packages.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Get the 3 newest revisions
dataPackageUploads <- list_recent_uploads("update", 3)
} # }
```
