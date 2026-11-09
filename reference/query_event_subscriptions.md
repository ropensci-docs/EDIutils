# Query event subscriptions

Query event subscriptions

## Usage

``` r
query_event_subscriptions(query = NULL, as = "data.frame", env = "production")
```

## Arguments

- query:

  (character) Query (see details below)

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) A list of the subscriptions whose
attributes match those specified in the query string (see details
below). If a query string is omitted, all subscriptions in the
subscription database will be returned for which the requesting user is
authorized to read. If query parameters are included, they are used to
filter that set of subscriptions based on their attributes.

## Details

Query parameters are specified as key=value pairs, multiple pairs must
be delimited with ampersands (&), and only a single value should be
specified for a particular key. The following query parameter keys are
allowed:

- creator

- scope

- identifier

- revision

- url

If a query parameter is specified, and a subscription's respective
attribute does not match it, that subscription will not be included in
the group of subscriptions returned. If scope, identifier, or revision
are used, their values must together constitute a syntactically and
semantically correct EML packageId (i.e. "scope.identifier.revision") -
either partial or complete. If url is used, its value must not contain
ampersands. Therefore, if a subscription's URL contains ampersands, it
cannot be filtered based on its URL.

## Note

User authentication is required (see
[`login()`](https://docs.ropensci.org/EDIutils/reference/login.md))

## See also

Other Event Notifications:
[`create_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/create_event_subscription.md),
[`delete_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/delete_event_subscription.md),
[`execute_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/execute_event_subscription.md),
[`get_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/get_event_subscription.md),
[`get_event_subscription_schema()`](https://docs.ropensci.org/EDIutils/reference/get_event_subscription_schema.md)

## Examples

``` r
if (FALSE) { # \dontrun{

login()

# Query subscriptions
query <- "scope=edi"
subscriptions <- query_event_subscriptions(query, env = "staging")

logout()
} # }
```
