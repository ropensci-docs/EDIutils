# Is authorized to read

Is authorized to read

## Usage

``` r
is_authorized(resourceId, env = "production")
```

## Arguments

- resourceId:

  (character) Resource identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(logical) TRUE if the authenticated user has permission to read the
specified resource

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Miscellaneous:
[`create_data_package_archive()`](https://docs.ropensci.org/EDIutils/reference/create_data_package_archive.md),
[`create_dn()`](https://docs.ropensci.org/EDIutils/reference/create_dn.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Get the most recently created data package
auditReport <- get_recent_uploads(
  query = "serviceMethod=createDataPackage&limit=1"
)

# Get the resourceId
resourceId <- xml2::xml_text(
  xml2::xml_find_all(auditReport, ".//resourceId")
)
resourceId
#> [1] "https://pasta.lternet.edu/package/eml/knb-lter-hbr/345/1"

# Check read authorization
is_authorized(resourceId)
#> [1] TRUE

logout()
} # }
```
