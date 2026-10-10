# Read evaluate report

Read evaluate report

## Usage

``` r
read_evaluate_report(transaction, as = "xml", env = "production")
```

## Arguments

- transaction:

  (character) Transaction identifier

- as:

  (character) Format of the returned report. Can be: "xml", "html", or
  "char".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(xml_document or html_document or character) The evaluate quality report
document

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Accessing:
[`read_data_entity()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity.md),
[`read_data_entity_checksum()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_checksum.md),
[`read_data_entity_name()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_name.md),
[`read_data_entity_names()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_names.md),
[`read_data_entity_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_resource_metadata.md),
[`read_data_entity_size()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_size.md),
[`read_data_entity_sizes()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_sizes.md),
[`read_data_package()`](https://docs.ropensci.org/EDIutils/reference/read_data_package.md),
[`read_data_package_archive()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_archive.md),
[`read_data_package_citation()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_citation.md),
[`read_data_package_doi()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_doi.md),
[`read_data_package_error()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_error.md),
[`read_data_package_from_doi()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_from_doi.md),
[`read_data_package_report()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_report.md),
[`read_data_package_report_checksum()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_report_checksum.md),
[`read_data_package_report_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_report_resource_metadata.md),
[`read_data_package_report_summary()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_report_summary.md),
[`read_data_package_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_resource_metadata.md),
[`read_evaluate_report_summary()`](https://docs.ropensci.org/EDIutils/reference/read_evaluate_report_summary.md),
[`read_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_metadata.md),
[`read_metadata_checksum()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_checksum.md),
[`read_metadata_dublin_core()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_dublin_core.md),
[`read_metadata_entity()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_entity.md),
[`read_metadata_format()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_format.md),
[`read_metadata_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_resource_metadata.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Evaluate data package
transaction <- evaluate_data_package(
  eml = paste0(tempdir(), "/edi.595.1.xml"),
  env = "staging"
)
transaction
#> [1] "evaluate_163966785813042760"

# Read as HTML and write to file for a web browser view
qualityReport <- read_evaluate_report(
  transaction = transaction,
  as = "html",
  env = "staging"
)
writeLines(qualityReport, paste0(tempdir(), "/report.html"))

# Read as character and write to file for browsing
qualityReport <- read_evaluate_report(
  transaction = transaction,
  as = "char",
  env = "staging"
)
writeLines(qualityReport, paste0(tempdir(), "/report.txt"))

# Read as XML
qualityReport <- read_evaluate_report(
  transaction = transaction,
  env = "staging"
)
qualityReport
#> {xml_document}
#> <qualityReport schemaLocation="eml://ecoinformatics.org/qualityReport ...
#> [1] <creationDate>2021-12-16T22:15:38</creationDate>
#> [2] <packageId>edi.606.1</packageId>
#> [3] <includeSystem>lter</includeSystem>
#> [4] <includeSystem>knb</includeSystem>
#> [5] <datasetReport>\n  <qualityCheck qualityType="metadata" system=" ...
#> [6] <entityReport>\n  <entityName>data.txt</entityName>\n  <qualityC ...

logout()
} # }
```
