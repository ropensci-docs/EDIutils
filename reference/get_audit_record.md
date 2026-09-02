# Get audit record

Get audit record

## Usage

``` r
get_audit_record(oid, as = "data.frame", env = "production")
```

## Arguments

- oid:

  (numeric) Audit identifier

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) An audit record

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Audit Manager Services:
[`get_audit_count()`](https://docs.ropensci.org/EDIutils/reference/get_audit_count.md),
[`get_audit_csv_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_csv_report.md),
[`get_audit_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_report.md),
[`get_docid_reads()`](https://docs.ropensci.org/EDIutils/reference/get_docid_reads.md),
[`get_packageid_reads()`](https://docs.ropensci.org/EDIutils/reference/get_packageid_reads.md),
[`get_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/get_recent_uploads.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Get audit report
auditReport <- get_audit_record(oid = "121606334")

logout()
} # }
```
