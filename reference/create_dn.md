# Create a users distinguished name (defunct)

This function is defunct. Distinguished names are deprecated in favor of
EDI IDs. An EDI ID can be obtained from the EDI Identity and Access
Manager (<https://auth.edirepository.org/auth/ui/signin>).

## Usage

``` r
create_dn(userId, ou = "EDI")
```

## Arguments

- userId:

  (character) User identifier of an EDI data repository account

- ou:

  (character) Organizational unit in which `userId` belongs. Can be
  "EDI" or "LTER". All `userId` issued after "2020-05-01" have
  `ou = "EDI"`.

## Value

(character) Distinguished name

## See also

Other Miscellaneous:
[`create_data_package_archive()`](https://docs.ropensci.org/EDIutils/reference/create_data_package_archive.md),
[`is_authorized()`](https://docs.ropensci.org/EDIutils/reference/is_authorized.md)

## Examples

``` r
if (FALSE) { # \dontrun{
# For an EDI account
dn <- create_dn(userId = "my_userid", ou = "EDI")
dn

# For an LTER account
dn <- create_dn(userId = "my_userid", ou = "LTER")
dn
} # }
```
