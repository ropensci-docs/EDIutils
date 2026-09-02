# Get package ID reads

Get package ID reads

## Usage

``` r
get_packageid_reads(packageId, as = "data.frame", env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) Summary of all the successful reads (total
reads and non-robot reads) of `packageId`

## See also

Other Audit Manager Services:
[`get_audit_count()`](https://docs.ropensci.org/EDIutils/reference/get_audit_count.md),
[`get_audit_csv_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_csv_report.md),
[`get_audit_record()`](https://docs.ropensci.org/EDIutils/reference/get_audit_record.md),
[`get_audit_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_report.md),
[`get_docid_reads()`](https://docs.ropensci.org/EDIutils/reference/get_docid_reads.md),
[`get_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/get_recent_uploads.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Get packageId reads
resourceReads <- get_packageid_reads("knb-lter-sgs.817.17")
} # }
```
