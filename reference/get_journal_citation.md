# Get journal citation

Get journal citation

## Usage

``` r
get_journal_citation(journalCitationId, as = "data.frame", env = "production")
```

## Arguments

- journalCitationId:

  (numeric) Journal citation identifier

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) Journal citation

## See also

Other Journal Citations:
[`create_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/create_journal_citation.md),
[`delete_journal_citation()`](https://docs.ropensci.org/EDIutils/reference/delete_journal_citation.md),
[`list_data_package_citations()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_citations.md),
[`list_principal_owner_citations()`](https://docs.ropensci.org/EDIutils/reference/list_principal_owner_citations.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Get citation
journalCitation <- get_journal_citation(381)
} # }
```
