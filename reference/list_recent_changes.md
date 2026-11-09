# List recent changes

List all data package insert, update, and delete operations, optionally
specifying the date and time to and/or from which the changes should be
listed. An optional scope value can be specified to filter results for a
particular data package scope.

## Usage

``` r
list_recent_changes(
  fromDate = NULL,
  toDate = NULL,
  scope = NULL,
  as = "data.frame",
  env = "production"
)
```

## Arguments

- fromDate:

  (character) Start date in the format "YYYY-MM-DDThh:mm:ss"

- toDate:

  (character) End date in the format "YYYY-MM-DDThh:mm:ss"

- scope:

  (character) Scope of data package

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) Recent changes and their corresponding
packageId, scope, identifier, revision, principal, doi, serviceMethod,
and date.

## See also

Other Listing:
[`list_data_descendants()`](https://docs.ropensci.org/EDIutils/reference/list_data_descendants.md),
[`list_data_entities()`](https://docs.ropensci.org/EDIutils/reference/list_data_entities.md),
[`list_data_package_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_identifiers.md),
[`list_data_package_revisions()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_revisions.md),
[`list_data_package_scopes()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_scopes.md),
[`list_data_sources()`](https://docs.ropensci.org/EDIutils/reference/list_data_sources.md),
[`list_deleted_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_deleted_data_packages.md),
[`list_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/list_recent_uploads.md),
[`list_service_methods()`](https://docs.ropensci.org/EDIutils/reference/list_service_methods.md),
[`list_user_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_user_data_packages.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Changes occurring in the first 3 days of 2021 for all scopes
dataPackageChanges <- list_recent_changes(
 fromDate = "2021-01-01T00:00:00",
 toDate = "2021-01-03T00:00:00"
)
} # }
```
