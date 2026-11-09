# Create data package archive (zip)

This function is DEPRECATED.

## Usage

``` r
create_data_package_archive(packageId, env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

transaction (character) Transaction identifier.

## See also

Other Miscellaneous:
[`create_dn()`](https://docs.ropensci.org/EDIutils/reference/create_dn.md),
[`is_authorized()`](https://docs.ropensci.org/EDIutils/reference/is_authorized.md)
