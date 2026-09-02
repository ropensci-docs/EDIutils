# List reservation identifiers

List reservation identifiers

## Usage

``` r
list_reservation_identifiers(scope, env = "production")
```

## Arguments

- scope:

  (character) Scope of data package

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) The set of identifiers for the specified `scope` that end
users have actively reserved for future upload

## See also

Other Identifier Reservations:
[`create_reservation()`](https://docs.ropensci.org/EDIutils/reference/create_reservation.md),
[`delete_reservation()`](https://docs.ropensci.org/EDIutils/reference/delete_reservation.md),
[`list_active_reservations()`](https://docs.ropensci.org/EDIutils/reference/list_active_reservations.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List reservations
reservations <- list_reservation_identifiers(scope = "edi")
reservations
#>   [1]   11  130  131  132  142  152  154  156  158  159  161  162  171
#>  [14]  172  173  174  175  177  178  180  182  183  185  196  203  ...
} # }
```
