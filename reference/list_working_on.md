# List working on

List working on

## Usage

``` r
list_working_on(as = "data.frame", env = "production")
```

## Arguments

- as:

  (character) Format of the returned object. Can be: "data.frame" or
  "xml".

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(data.frame or xml_document) The set of data packages the EDI repository
is currently working on inserting or updating. Note that data packages
currently being evaluated by the EDI repository are not included in the
list.

## Examples

``` r
if (FALSE) { # \dontrun{

list_working_on()
} # }
```
