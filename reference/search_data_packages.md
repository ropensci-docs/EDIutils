# Search data packages

Searches data packages in the EDI data repository using the specified
Solr query.

## Usage

``` r
search_data_packages(query, as = "data.frame", env = "production")
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

(data.frame or xml_document) Search results containing the fields:

- abstract

- begindate

- doi

- enddate

- funding

- geographicdescription

- id

- methods

- packageid

- pubdate

- responsibleParties

- scope

- site

- taxonomic

- title

- authors

- spatialCoverage

- sources

- keywords

- organizations

- singledates

- timescales

## Details

Documents in the EDI data repository Solr index can be discovered based
on metadata values stored in the following list of searchable fields
(not all EML content is queryable):

Single-value fields:

- abstract

- begindate - In ISO format (YYYY-MM-DDThh:mm:ss)

- doi

- enddate - In ISO format (YYYY-MM-DDThh:mm:ss)

- funding

- geographicdescription

- id

- methods

- packageid - Data Id in "scope.identifier.revision" format

- pubdate - In ISO format (YYYY-MM-DDThh:mm:ss)

- responsibleParties

- scope

- singledate

- site

- taxonomic

- title

Multi-value fields:

- author

- coordinates - Use `"IsWithin(West+East+North+South)"` where each
  cardinal direction is in decimal degrees with South of the equator as
  negative and East of the prime meridian positive.

- keyword

- organization

- projectTitle

- relatedProjectTitle

- timescale

`query` parser: The optimal query parser (defType=edismax) is added to
every query.

See [Apache Solr
Wiki](https://cwiki.apache.org/confluence/display/solr/) for how to
construct a Solr query.

## Note

Only the newest version of data packages are searchable, older versions
are not.

When constructing a query note that the 15403 data packages of the
[ecotrends](https://lternet.edu/the-ecotrends-project/) project and
10492 data packages of the [LTER
Landsat](https://lternet.edu/lter-remote-sensing-and-geographic-information-system-data/)
project, can be excluded from the returned results by including
`&fq=-scope:(ecotrends+lter-landsat)` in the query string.

## Examples

``` r
if (FALSE) { # \dontrun{

# Search for data packages containing the term "air temperature"
res <- search_data_packages(query = 'q="air+temperature"&fl=*')

# Search for data packages containing the term "air temperature" and
# returning only the packageid, title, and score of each match
res <- search_data_packages(query = 'q="air+temperature"&fl=packageid,title,score')

# Search for data packages containing the term "air temperature", returning
# only the packageid, title, score, and excluding ecotrends and lter-landsat
# scopes from the returned results
query <- paste0('q="air+temperature"&fl=packageid,title,score&',
                'fq=-scope:(ecotrends+lter-landsat)')
res <- search_data_packages(query)
} # }
```
