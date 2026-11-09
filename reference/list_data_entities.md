# List data entities

List data entities

## Usage

``` r
list_data_entities(packageId, env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(character) Identifiers for all data entities in `packageId`

## See also

Other Listing:
[`list_data_descendants()`](https://docs.ropensci.org/EDIutils/reference/list_data_descendants.md),
[`list_data_package_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_identifiers.md),
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

entityIds <- list_data_entities("knb-lter-and.2732.7")
entityIds
#> [1] "0464a1d9262fc6e609cb0b24adb7e5ba"
#> [2] "cc3ade83d3655edd2ca674721a52ef46"
} # }
```
