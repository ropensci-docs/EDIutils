# Read data entity

Read data entity

## Usage

``` r
read_data_entity(packageId, entityId, env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- entityId:

  (character) Data entity identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(raw) Raw bytes (i.e. application/octet-stream) to be parsed by a reader
function appropriate for the data type

## See also

Other Accessing:
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
[`read_metadata_dublin_core()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_dublin_core.md),
[`read_metadata_entity()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_entity.md),
[`read_metadata_format()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_format.md),
[`read_metadata_resource_metadata()`](https://docs.ropensci.org/EDIutils/reference/read_metadata_resource_metadata.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Read names and IDs of data entities in package "edi.1047.1"
res <- read_data_entity_names(packageId = "edi.1047.1")
res
#>                           entityId                entityName
#> 1 3abac5f99ecc1585879178a355176f6d        Environmentals.csv
#> 2 f6bfa89b48ced8292840e53567cbf0c8               ByCatch.csv
#> 3 c75642ddccb4301327b4b1a86bdee906               Chinook.csv
#> 4 2c9ee86cc3f3ffc729c5f18bfe0a2a1d             Steelhead.csv
#> 5 785690848dd20f4910637250cdc96819 TrapEfficiencyRelease.csv
#> 6 58b9000439a5671ea7fe13212e889ba5 TrapEfficiencySummary.csv
#> 7 86e61c1a501b7dcf0040d10e009bfd87        TrapOperations.csv

# Read raw bytes of the 3rd data entity
raw <- read_data_entity(packageId = "edi.1047.1", entityId = res$entityId[3])
head(raw)
#> [1] ef bb bf 44 61 74

# Parse with .csv reader
data <- readr::read_csv(file = raw)
data
#> # A tibble: 105,325 x 20
#> Date   trapVisitID subSiteName  catchRawID releaseID commonName     n
#> <chr>        <dbl> <chr>             <dbl>     <dbl> <chr>      <dbl>
#>   1 1/8/2~         330 North Chann~      32409         0 Chinook s~     1
#> 2 1/8/2~         330 North Chann~      32412         0 Chinook s~     1
#> 3 1/8/2~         330 North Chann~      32410         0 Chinook s~     1
#> 4 1/8/2~         330 North Chann~      32408         0 Chinook s~     1
#> 5 1/8/2~         330 North Chann~      32406         0 Chinook s~     1
#> 6 1/8/2~         322 North Chann~      31958         0 Chinook s~     1
#> 7 1/8/2~         322 North Chann~      31975         0 Chinook s~     1
#> 8 1/8/2~         322 North Chann~      31974         0 Chinook s~     1
#> 9 1/8/2~         322 North Chann~      31973         0 Chinook s~     1
#> 10 1/8/2~         322 North Chann~      31972         0 Chinook s~     1
#> # ... with 105,315 more rows, and 13 more variables:
#> #   atCaptureRun <chr>, finalRun <chr>, finalRunMethod <chr>,
#> #   lifeStage <chr>, forkLength <dbl>, weight <dbl>, mort <chr>,
#> #   fishOrigin <chr>, markType <chr>, CatchRaw.comments <chr>,
#> #   specimenTypeID <dbl>, physicalSpecimenCode <chr>,
#> #   Specimen.comments <lgl>
} # }
```
