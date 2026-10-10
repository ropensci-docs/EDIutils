# Get event subscription

Get event subscription

## Usage

``` r
get_event_subscription(subscriptionId, as = "data.frame", env = "production")
```

## Arguments

- subscriptionId:

  (numeric) Event subscription identifier

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) Subscription metadata

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Event Notifications:
[`create_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/create_event_subscription.md),
[`delete_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/delete_event_subscription.md),
[`execute_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/execute_event_subscription.md),
[`get_event_subscription_schema()`](https://docs.ropensci.org/EDIutils/reference/get_event_subscription_schema.md),
[`query_event_subscriptions()`](https://docs.ropensci.org/EDIutils/reference/query_event_subscriptions.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Get subscription
subscription <- get_event_subscription(
  subscriptionId = 21,
  env = "staging"
)

logout()
} # }
```
