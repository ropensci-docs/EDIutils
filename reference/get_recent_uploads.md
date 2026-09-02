# Get recent uploads

Get recent uploads

## Usage

``` r
get_recent_uploads(query, as = "data.frame", env = "production")
```

## Arguments

- query:

  (character) Query (see details below)

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) A list of zero or more audit records of
either recently inserted or recently updated data packages.

## Details

Query parameters are specified as key=value pairs, multiple pairs must
be delimited with ampersands (&), and only a single value should be
specified for a particular key. The following query parameter keys are
allowed:

- serviceMethod - Can be: createDataPackage, updateDataPackage

- fromTime - An ISO8601 timestamp

- limit - A positive whole number

The query parameter serviceMethod should have the value
"createDataPackage" (to retrieve recent inserts) or "updateDataPackage"
(to retrieve recent updates). The query parameter fromTime is used to
specify the date/time in the past that represents the oldest audit
records that should be returned. Data packages uploaded prior to that
time are not considered recent uploads and are thus filtered from the
query results. The query parameter limit sets an upper limit on the
number of audit records returned. For example, "limit=3".

## See also

Other Audit Manager Services:
[`get_audit_count()`](https://docs.ropensci.org/EDIutils/reference/get_audit_count.md),
[`get_audit_csv_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_csv_report.md),
[`get_audit_record()`](https://docs.ropensci.org/EDIutils/reference/get_audit_record.md),
[`get_audit_report()`](https://docs.ropensci.org/EDIutils/reference/get_audit_report.md),
[`get_docid_reads()`](https://docs.ropensci.org/EDIutils/reference/get_docid_reads.md),
[`get_packageid_reads()`](https://docs.ropensci.org/EDIutils/reference/get_packageid_reads.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Get the 5 most recently created data packages
auditReport <- get_recent_uploads(
 query = "serviceMethod=createDataPackage&limit=5"
)
} # }
```
