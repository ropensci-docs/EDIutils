# Delete journal citation

Delete journal citation

## Usage

``` r
delete_journal_citation(journalCitationId, env = "production")
```

## Arguments

- journalCitationId:

  (numeric) Journal citation identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(logical) TRUE if deleted

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Journal Citations:
[`create_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/create_journal_citation.md),
[`get_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/get_journal_citation.md),
[`list_data_package_citations()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_citations.md),
[`list_principal_owner_citations()`](https://docs.ropensci.org/EDIutils/reference/list_principal_owner_citations.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Create journal citation
journalCitationId <- create_journal_citation(
  packageId = "edi.17.1",
  articleDoi = "https://doi.org/10.1890/11-1026.1",
  articleTitle = "Corridors promote fire via connectivity and edge effects",
  journalTitle = "Ecological Applications",
  relationType = "IsCitedBy",
  env = "staging"
)
journalCitationId
#> [1] 74

# Delete journal citation
delete_journal_citation(journalCitationId, env = "staging")
#> [1] TRUE

logout()
} # }
```
