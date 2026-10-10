# Check data package creation status

Check data package creation status

## Usage

``` r
check_status_create(transaction, wait = TRUE, env = "production")
```

## Arguments

- transaction:

  (character) Transaction identifier

- wait:

  (logical) Wait for evaluation to complete? See details below.

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(logical) TRUE if creation has completed, FALSE if in progress, and
error if an error was encountered while processing the request

## Details

If `wait = TRUE`, then the function will enter a "while" loop checking
every 2 seconds for the completed evaluation report. If `wait = FALSE`,
then the function will only check once and return the result.

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Evaluation and Upload:
[`check_status_evaluate()`](https://docs.ropensci.org/EDIutils/reference/check_status_evaluate.md),
[`check_status_update()`](https://docs.ropensci.org/EDIutils/reference/check_status_update.md),
[`create_data_package()`](https://docs.ropensci.org/EDIutils/reference/create_data_package.md),
[`evaluate_data_package()`](https://docs.ropensci.org/EDIutils/reference/evaluate_data_package.md),
[`update_data_package()`](https://docs.ropensci.org/EDIutils/reference/update_data_package.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Create data package
transaction <- create_data_package(
  eml = paste0(tempdir(), "/edi.595.1.xml"),
  env = "staging"
)
transaction
#> [1] "create_163966765080210573__edi.595.1"

# Check creation status
status <- check_status_create(
  transaction = transaction,
  env = "staging"
)
status
#> [1] TRUE

logout()
} # }
```
