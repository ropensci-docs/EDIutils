# Read data package report

Read data package report

## Usage

``` r
read_data_package_report(packageId, as = "xml", env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- as:

  (character) Format of the returned report. Can be: "xml", "html", or
  "char".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(xml_document) Data package report

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
[`read_data_package_report_checksum()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_report_checksum.md),
[`read_data_package_report_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_report_resource_metadata.md),
[`read_data_package_report_summary()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_report_summary.md),
[`read_data_package_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_data_package_resource_metadata.md),
[`read_evaluate_report()`](https://docs.ropensci.org/EDIutils/reference/read_evaluate_report.md),
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

# Read as XML
qualityReport <- read_data_package_report("knb-lter-knz.260.4")
qualityReport
#> {xml_document}
#> <qualityReport schemaLocation="eml://ecoinformatics.org/qualityReport ...
#>  [1] <creationDate>2020-02-04T16:38:38</creationDate>
#>  [2] <packageId>knb-lter-knz.260.4</packageId>
#>  [3] <includeSystem>lter</includeSystem>
#>  [4] <includeSystem>knb</includeSystem>
#>  [5] <datasetReport>\n  <qualityCheck qualityType="metadata" system=" ...
#>  [6] <entityReport>\n  <entityName>GIS600</entityName>\n  <qualityChe ...
#>  [7] <entityReport>\n  <entityName>KMZGIS600</entityName>\n  <quality ...
#>  [8] <entityReport>\n  <entityName>GIS605</entityName>\n  <qualityChe ...
#>  [9] <entityReport>\n  <entityName>KMZGIS605</entityName>\n  <quality ...
#> [10] <entityReport>\n  <entityName>GIS610</entityName>\n  <qualityChe ...
#> ...

# Read as HTML
qualityReport <- read_data_package_report(
 packageId = "knb-lter-knz.260.4",
 as = "html"
)
qualityReport
#> {html_document}
#> <html>
#> [1] <body><table xmlns:qr="eml://ecoinformatics.org/qualityReport"><t ...

# Read as character
qualityReport <- read_data_package_report(
 packageId = "knb-lter-knz.260.4",
 as = "char"
)
# writeLines(qualityReport, paste0(tempdir(), "/report.txt"))
} # }
```
