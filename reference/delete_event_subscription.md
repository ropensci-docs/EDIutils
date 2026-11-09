# Delete event subscription

Delete event subscription

## Usage

``` r
delete_event_subscription(subscriptionId, env = "production")
```

## Arguments

- subscriptionId:

  (numeric) Event subscription identifier

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(logical) TRUE if the event subscription was deleted

## Details

After "deletion", the subscription might still exist in the subscription
database, but it will be inactive - it will not conflict with future
creation requests, it cannot be read, and it will not be notified of
events.

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Event Notifications:
[`create_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/create_event_subscription.md),
[`execute_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/execute_event_subscription.md),
[`get_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/get_event_subscription.md),
[`get_event_subscription_schema()`](https://docs.ropensci.org/EDIutils/reference/get_event_subscription_schema.md),
[`query_event_subscriptions()`](https://docs.ropensci.org/EDIutils/reference/query_event_subscriptions.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Create subscription
subscriptionId <- create_event_subscription(
  packageId = "knb-lter-vcr.340.1",
  url = "https://my.webserver.org/",
  env = "staging"
)
subscriptionId
#> [1] 48

# Execute subscription
execute_event_subscription(
  subscriptionId = subscriptionId,
  env = "staging"
)
#> [1] TRUE

# Delete subscription
delete_event_subscription(subscriptionId, env = "staging")
#> [1] TRUE

logout()
} # }
```
