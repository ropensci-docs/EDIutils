# Read metadata Dublin Core

Read metadata Dublin Core

## Usage

``` r
read_metadata_dublin_core(packageId, env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(xml_document) Dublin Core metadata.

See the [xml2](https://CRAN.R-project.org/package=xml2) library for more
on working with XML.

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
[`read_evaluate_report()`](https://docs.ropensci.org/EDIutils/reference/read_evaluate_report.md),
[`read_evaluate_report_summary()`](https://docs.ropensci.org/EDIutils/reference/read_evaluate_report_summary.md),
[`read_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_metadata.md),
[`read_metadata_checksum()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_checksum.md),
[`read_metadata_entity()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_entity.md),
[`read_metadata_format()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_format.md),
[`read_metadata_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_resource_metadata.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Read dc metadata
dc <- read_metadata_dublin_core("knb-lter-nes.10.1")
dc
#> {xml_document}
#> <dc schemaLocation="http://www.openarchives.org/OAI/2.0/oai_dc/ http: ...
#> [1] <dc:type/>
#> [2] <dc:identifier/>
} # }
```
