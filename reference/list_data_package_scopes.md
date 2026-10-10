# List data package scopes

List data package scopes

## Usage

``` r
list_data_package_scopes(env = "production")
```

## Arguments

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) Scopes within a specified `env`

## See also

Other Listing:
[`list_data_descendants()`](https://docs.ropensci.org/EDIutils/reference/list_data_descendants.md),
[`list_data_entities()`](https://docs.ropensci.org/EDIutils/reference/list_data_entities.md),
[`list_data_package_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_identifiers.md),
[`list_data_package_revisions()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_revisions.md),
[`list_data_sources()`](https://docs.ropensci.org/EDIutils/reference/list_data_sources.md),
[`list_deleted_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_deleted_data_packages.md),
[`list_recent_changes()`](https://docs.ropensci.org/EDIutils/reference/list_recent_changes.md),
[`list_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/list_recent_uploads.md),
[`list_service_methods()`](https://docs.ropensci.org/EDIutils/reference/list_service_methods.md),
[`list_user_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_user_data_packages.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List scopes
scopes <- list_data_package_scopes()
scopes
#>  [1] "ecotrends"           "edi"                 "knb-lter-and"       
#>  [4] "knb-lter-arc"        "knb-lter-bes"        "knb-lter-ble"       
#>  [7] "knb-lter-bnz"        "knb-lter-cap"        "knb-lter-cce"       
#> [10] "knb-lter-cdr"        "knb-lter-cwt"        "knb-lter-fce"       
#> [13] "knb-lter-gce"        "knb-lter-hbr"        "knb-lter-hfr"       
#> [16] "knb-lter-jrn"        "knb-lter-kbs"        "knb-lter-knz"       
#> [19] "knb-lter-luq"        "knb-lter-mcm"        "knb-lter-mcr"       
#> [22] "knb-lter-nes"        "knb-lter-nin"        "knb-lter-ntl"       
#> [25] "knb-lter-nwk"        "knb-lter-nwt"        "knb-lter-pal"       
#> [28] "knb-lter-pie"        "knb-lter-sbc"        "knb-lter-sev"       
#> [31] "knb-lter-sgs"        "knb-lter-vcr"        "lter-landsat"       
#> [34] "lter-landsat-ledaps" "msb-cap"             "msb-paleon"         
#> [37] "msb-tempbiodev"   
} # }
```
