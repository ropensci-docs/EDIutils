# List data package identifiers

List data package identifiers

## Usage

``` r
list_data_package_identifiers(scope, env = "production")
```

## Arguments

- scope:

  (character) Scope of data package

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) Identifiers of data packages within a specified `scope`

## See also

Other Listing:
[`list_data_descendants()`](https://docs.ropensci.org/EDIutils/reference/list_data_descendants.md),
[`list_data_entities()`](https://docs.ropensci.org/EDIutils/reference/list_data_entities.md),
[`list_data_package_revisions()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_revisions.md),
[`list_data_package_scopes()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_scopes.md),
[`list_data_sources()`](https://docs.ropensci.org/EDIutils/reference/list_data_sources.md),
[`list_deleted_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_deleted_data_packages.md),
[`list_recent_changes()`](https://docs.ropensci.org/EDIutils/reference/list_recent_changes.md),
[`list_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/list_recent_uploads.md),
[`list_service_methods()`](https://docs.ropensci.org/EDIutils/reference/list_service_methods.md),
[`list_user_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_user_data_packages.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List identifiers
identifiers <- list_data_package_identifiers("knb-lter-ble")
identifiers
#> [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 23
} # }
```
