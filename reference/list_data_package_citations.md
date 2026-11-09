# List data package citations

List data package citations

## Usage

``` r
list_data_package_citations(
  packageId,
  as = "data.frame",
  list_all = FALSE,
  env = "production"
)
```

## Arguments

- packageId:

  (character) Data package identifier

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- list_all:

  (logical) Return all citations within a data package series?

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) A list of journal citations

## See also

Other Journal Citations:
[`create_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/create_journal_citation.md),
[`delete_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/delete_journal_citation.md),
[`get_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/get_journal_citation.md),
[`list_principal_owner_citations()`](https://docs.ropensci.org/EDIutils/reference/list_principal_owner_citations.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List citations
journalCitations <- list_data_package_citations("edi.845.1")
} # }
```
