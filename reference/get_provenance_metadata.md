# Get provenance metadata

Generates the provenance metadata of a source data package

## Usage

``` r
get_provenance_metadata(packageId, env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(xml_document) Provenance metadata of `packageId`, representing a
\<methodStep\> element that can be inserted into the \<methods\> section
of a dependent data package.

See the [emld](https://CRAN.R-project.org/package=emld) library for more
on working with EML as a list or JSON-LD. See the
[xml2](https://CRAN.R-project.org/package=xml2) library for working with
EML as XML.

## Examples

``` r
if (FALSE) { # \dontrun{

methodStep <- get_provenance_metadata("knb-lter-pal.309.1")
methodStep
#> {xml_document}
#> <methodStep>
#> [1] <description>\n  <para>This method step describes provenance-based ...
#> [2] <dataSource>\n  <title>Stable isotope composition (d18O) of seawat ...
} # }
```
