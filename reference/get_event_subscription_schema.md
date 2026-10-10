# Get event subscription schema

Get event subscription schema

## Usage

``` r
get_event_subscription_schema(env = "production")
```

## Arguments

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(xml_document) Schema for event subscription creation request entities.

See the [xml2](https://CRAN.R-project.org/package=xml2) library for more
on working with XML.

## See also

Other Event Notifications:
[`create_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/create_event_subscription.md),
[`delete_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/delete_event_subscription.md),
[`execute_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/execute_event_subscription.md),
[`get_event_subscription()`](https://docs.ropensci.org/EDIutils/reference/get_event_subscription.md),
[`query_event_subscriptions()`](https://docs.ropensci.org/EDIutils/reference/query_event_subscriptions.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Get schema
schema <- get_event_subscription_schema()
schema
#> {xml_document}
#> <schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
#> [1] <xs:element name="subscription">\n  <xs:complexType>\n    <xs:    ...

# Show schema structure
xml2::xml_structure(schema)
#> <schema [xmlns:xs]>
#>   <element [name]>
#>     <complexType>
#>       <all>
#>         <element [name, type, minOccurs, maxOccurs]>
#>         <element [name, type, minOccurs, maxOccurs]>
#>       <attribute [name, type, use, fixed]>
} # }
```
