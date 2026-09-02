# List user data packages

List all data packages (including their revision values) uploaded to the
repository by a particular user, specified by a distinguished name. Data
packages that were uploaded by the specified user but have since been
deleted are excluded from the list.

## Usage

``` r
list_user_data_packages(edi_id, env = "production")
```

## Arguments

- edi_id:

  (character) The EDI ID of the user. An EDI ID can be obtained from the
  EDI Identity and Access Manager
  (<https://auth.edirepository.org/auth/ui/signin>).

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(character) Data package identifiers belonging to a `edi_id`

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
[`list_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/list_recent_uploads.md),
[`list_service_methods()`](https://docs.ropensci.org/EDIutils/reference/list_service_methods.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List user data packages
edi_id <- "EDI-543afa80c859825d35d37d9111c24a4a65a0ff9e"
packageIds <- list_user_data_packages(edi_id)
packageIds
#> [1] "edi.948.1" "edi.949.1"
} # }
```
