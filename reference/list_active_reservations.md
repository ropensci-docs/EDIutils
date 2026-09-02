# List active reservations

List active reservations

## Usage

``` r
list_active_reservations(as = "data.frame", env = "production")
```

## Arguments

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) The set of data package identifiers that
users have actively reserved. Note that data package identifiers that
have been successfully uploaded are no longer considered active
reservations and thus are not included in this list.

## See also

Other Identifier Reservations:
[`create_reservation()`](https://docs.ropensci.org/EDIutils/reference/create_reservation.md),
[`delete_reservation()`](https://docs.ropensci.org/EDIutils/reference/delete_reservation.md),
[`list_reservation_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_reservation_identifiers.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# List reservations
reservations <- list_active_reservations()
} # }
```
