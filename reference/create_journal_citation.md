# Create journal citation

Create journal citation

## Usage

``` r
create_journal_citation(
  packageId,
  articleDoi = NULL,
  articleUrl = NULL,
  articleTitle = NULL,
  journalTitle = NULL,
  relationType,
  env = "production"
)
```

## Arguments

- packageId:

  (character) Data package identifier

- articleDoi:

  (character) Article DOI. Required if `articleUrl` is missing.

- articleUrl:

  (character) Article URL. Required if `articleDoi` is missing.

- articleTitle:

  (character) Article title

- journalTitle:

  (character) Journal title

- relationType:

  (character) Relation between citation and data package. Can be:
  "IsCitedBy" this data package is formally cited in the manuscript;
  "IsDescribedBy" - this data package is explicitly described within the
  manuscript; "IsReferencedBy" - this data package is implicitly
  described within the manuscript.

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) Journal citation identifier

## Details

Creates a new journal citation entry in the EDI data repository

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Journal Citations:
[`delete_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/delete_journal_citation.md),
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
  articleDoi = "10.1890/11-1026.1",
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
