# Create reservation

Reserves the next available identifier for the specified scope

## Usage

``` r
create_reservation(scope, env = "production")
```

## Arguments

- scope:

  (character) Scope of data package

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) Identifier of reserved data package

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Identifier Reservations:
[`delete_reservation()`](https://docs.ropensci.org/EDIutils/reference/delete_reservation.md),
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
