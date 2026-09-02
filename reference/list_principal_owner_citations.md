# List principal owner citations

List principal owner citations

## Usage

``` r
list_principal_owner_citations(
  principalOwner,
  as = "data.frame",
  env = "production"
)
```

## Arguments

- principalOwner:

  (character) The EDI ID of the principal owner. EDI IDs can be obtained
  from the EDI Identity and Access Manager
  (<https://auth.edirepository.org/auth/ui/signin>).

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) Journal citations metadata for all entries
owned by the specified principal owner

## See also

Other Journal Citations:
[`create_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/create_journal_citation.md),
[`delete_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/delete_journal_citation.md),
[`get_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/get_journal_citation.md),
[`list_data_package_citations()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_citations.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List citations
edi_id <- "EDI-543afa80c859825d35d37d9111c24a4a65a0ff9e"
journalCitations <- list_principal_owner_citations(principalOwner = edi_id)
} # }
```
