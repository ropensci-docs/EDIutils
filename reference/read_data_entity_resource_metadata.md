# Read data entity resource metadata

Read data entity resource metadata

## Usage

``` r
read_data_entity_resource_metadata(
  packageId,
  entityId,
  as = "data.frame",
  env = "production"
)
```

## Arguments

- packageId:

  (character) Data package identifier

- entityId:

  (character) Data entity identifier

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) The resource metadata of `entityId` in
`packageId`

## See also

Other Accessing:
[`read_data_entity()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity.md),
[`read_data_entity_checksum()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_checksum.md),
[`read_data_entity_name()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_name.md),
[`read_data_entity_names()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_names.md),
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
[`read_metadata_dublin_core()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_dublin_core.md),
[`read_metadata_entity()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_entity.md),
[`read_metadata_format()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_format.md),
[`read_metadata_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_resource_metadata.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List entities
entityIds <- list_data_entities(packageId = "knb-lter-cce.310.1")
head(entityIds)
#> [1] "4aaaff61e0d316130be0b445d3013877"
#> [2] "088775341e7fb65206af8c9e67d076e2"
#> [3] "6982dd80cba66470c49a2f3dc0f82459"
#> [4] "782fbaa20ea62987c838378e9eadcfa6"
#> [5] "ae8ecd148df1275b30358577d0fa6b4a"
#> [6] "a53b312efe0a176fdfc74ab7ccb0916b"

# Read resource metadata for first entity
resourceMetadata <- read_data_entity_resource_metadata(
 packageId = "knb-lter-cce.310.1",
 entityId = entityIds[1]
)
} # }
```
