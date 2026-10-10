# List data package revisions

List data package revisions

## Usage

``` r
list_data_package_revisions(
  scope,
  identifier,
  filter = NULL,
  env = "production"
)
```

## Arguments

- scope:

  (character) Scope of data package

- identifier:

  (numeric) Identifier of data package

- filter:

  (character) Filter results by "newest" or "oldest"

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) Revisions of a data package within a specified `scope` and
`identifier`

## See also

Other Listing:
[`list_data_descendants()`](https://docs.ropensci.org/EDIutils/reference/list_data_descendants.md),
[`list_data_entities()`](https://docs.ropensci.org/EDIutils/reference/list_data_entities.md),
[`list_data_package_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_identifiers.md),
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

# List revisions
revisions <- list_data_package_revisions("knb-lter-arc", 20131)
revisions
#> [1] 1 2
} # }
```
