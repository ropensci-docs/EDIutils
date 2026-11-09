# Delete reservation

Delete reservation

## Usage

``` r
delete_reservation(scope, identifier, env = "production")
```

## Arguments

- scope:

  (character) Scope of data package

- identifier:

  (numeric) Identifier of data package

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) The deleted reservation identifier value

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md)). The
same user who originally authenticated to create the reservation must
authenticate to delete it.

## See also

Other Identifier Reservations:
[`create_reservation()`](https://docs.ropensci.org/EDIutils/reference/create_reservation.md),
[`list_active_reservations()`](https://docs.ropensci.org/EDIutils/reference/list_active_reservations.md),
[`list_reservation_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_reservation_identifiers.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Create reservation
identifier <- create_reservation(scope = "edi", env = "staging")
identifier
#> [1] 604

# Delete reservation
delete_reservation(scope = "edi", identifier = identifier, env = "staging")
#> [1] 604

logout()
} # }
```
