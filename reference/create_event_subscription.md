# Create event subscription

Create event subscription

## Usage

``` r
create_event_subscription(packageId, url, env = "production")
```

## Arguments

- packageId:

  (character) Data package identifier

- url:

  (character) Where the event notification will be sent

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(numeric) Event subscription identifier

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

The `url` must have "http" as its scheme and must be able to receive
POST requests with MIME type text/plain. Additionally, because the `url`
will be passed in an XML body, some characters must be escaped, such as
ampersands from & to &amp;.

## See also

Other Event Notifications:
[`delete_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/delete_event_subscription.md),
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
execute_event_subscription(subscriptionId, env = "staging")
#> [1] TRUE

# Delete subscription
delete_event_subscription(subscriptionId, env = "staging")
#> [1] TRUE

logout()
} # }
```
