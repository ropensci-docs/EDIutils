# Get doc ID reads

Get doc ID reads

## Usage

``` r
get_docid_reads(scope, identifier, as = "data.frame", env = "production")
```

## Arguments

- scope:

  (character) Scope of data package

- identifier:

  (numeric) Identifier of data package

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) Summary of all the successful reads (total
reads and non-robot reads) for all the resources of a given `scope` and
`identifier`.

## See also

Other Audit Manager Services:
[`get_audit_count()`](https://docs.ropensci.org/EDIutils/reference/get_audit_count.md),
[`get_audit_csv_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_csv_report.md),
[`get_audit_record()`](https://docs.ropensci.org/EDIutils/reference/get_audit_record.md),
[`get_audit_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_report.md),
[`get_packageid_reads()`](https://docs.ropensci.org/EDIutils/reference/get_packageid_reads.md),
[`get_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/get_recent_uploads.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Get all reads
resourceReads <- get_docid_reads(scope = "knb-lter-sgs", identifier = 817)
} # }
```
