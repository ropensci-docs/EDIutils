# Read data package

Read data package

## Usage

``` r
read_data_package(packageId, ore = FALSE, env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- ore:

  (logical) Return an OAI-ORE compliant resource map in RDF-XML format

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(character or xml_document) A resource map with reference URLs to each
of the metadata, data, and quality report resources that comprise the
`packageId`.

## See also

Other Accessing:
[`read_data_entity()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity.md),
[`read_data_entity_checksum()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_checksum.md),
[`read_data_entity_name()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_name.md),
[`read_data_entity_names()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_names.md),
[`read_data_entity_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_resource_metadata.md),
[`read_data_entity_size()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_size.md),
[`read_data_entity_sizes()`](https://docs.ropensci.org/EDIutils/reference/read_data_entity_sizes.md),
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
# Get resource map
resourceMap <- read_data_package(packageId = "knb-lter-cwt.5026.13")
resourceMap
#> [1] "https://pasta.lternet.edu/package/data/eml/knb-lter-cwt/5026/13/ ...
#> [2] "https://pasta.lternet.edu/package/data/eml/knb-lter-cwt/5026/13/ ...
#> [3] "https://pasta.lternet.edu/package/metadata/eml/knb-lter-cwt/5026 ...
#> [4] "https://pasta.lternet.edu/package/report/eml/knb-lter-cwt/5026/1 ...
#> [5] "https://pasta.lternet.edu/package/eml/knb-lter-cwt/5026/13" 

# Get resource map in ORE format
resourceMap <- read_data_package(
 packageId = "knb-lter-cwt.5026.13",
 ore = TRUE
)
resourceMap
#> {xml_document}
#> <RDF xmlns:cito="http://purl.org/spar/cito/" xmlns:dc="http://purl.or ...
#> [1] <rdf:Description rdf:about="https://pasta.lternet.edu/package/eml ...
#> [2] <rdf:Description rdf:about="https://pasta.lternet.edu/package/eml ...
#> [3] <rdf:Description rdf:about="https://pasta.lternet.edu/package/eml ...
#> [4] <rdf:Description rdf:about="https://pasta.lternet.edu/package/eml ...
#> [5] <rdf:Description rdf:about="https://pasta.lternet.edu/package/eml ...
#> [6] <rdf:Description rdf:about="https://pasta.lternet.edu/package/eml ...
#> [7] <rdf:Description rdf:about="http://environmentaldatainitiative.or ...
#> [8] <rdf:Description rdf:about="http://www.openarchives.org/ore/terms ...
#> [9] <rdf:Description rdf:about="http://www.openarchives.org/ore/terms ...
} # }
```
