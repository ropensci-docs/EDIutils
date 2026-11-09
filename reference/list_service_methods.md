# List service methods

List service methods

## Usage

``` r
list_service_methods(env = "production")
```

## Arguments

- env:

  (character) Repository environment. Can be: "production", "staging",
  or "development".

## Value

(character) A simple list of web service methods supported by the Data
Package Manager web service

## See also

Other Listing:
[`list_data_descendants()`](https://docs.ropensci.org/EDIutils/reference/list_data_descendants.md),
[`list_data_entities()`](https://docs.ropensci.org/EDIutils/reference/list_data_entities.md),
[`list_data_package_identifiers()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_identifiers.md),
[`list_data_package_revisions()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_revisions.md),
[`list_data_package_scopes()`](https://docs.ropensci.org/EDIutils/reference/list_data_package_scopes.md),
[`list_data_sources()`](https://docs.ropensci.org/EDIutils/reference/list_data_sources.md),
[`list_deleted_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_deleted_data_packages.md),
[`list_recent_changes()`](https://docs.ropensci.org/EDIutils/reference/list_recent_changes.md),
[`list_recent_uploads()`](https://docs.ropensci.org/EDIutils/reference/list_recent_uploads.md),
[`list_user_data_packages()`](https://docs.ropensci.org/EDIutils/reference/list_user_data_packages.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# All service methods
services <- list_service_methods()
services
#>  [1] "appendProvenance"              "createDataPackage"            
#>  [3] "createDataPackageArchive"      "createReservation"            
#>  [5] "deleteReservation"             "deleteDataPackage"            
#>  [7] "evaluateDataPackage"           "getProvenanceMetadata"        
#>  [9] "isAuthorized"                  "listActiveReservations"       
#> [11] "listDataEntities"              "listDataDescendants"          
#> [13] "listDataSources"               "listRecentChanges"            
#> [15] "listDataPackageIdentifiers"    "listDataPackageRevisions"     
#> [17] "listDataPackageScopes"         "listDeletedDataPackages"      
#> [19] "listRecentUploads"             "listReservationIdentifiers"   
#> [21] "listServiceMethods"            "listUserDataPackages"         
#> [23] "listWorkingOn"                 "readDataEntity"               
#> [25] "readDataEntityAcl"             "readDataEntityRmd"            
#> [27] "readDataEntityChecksum"        "readDataEntityDoi"            
#> [29] "readDataEntityName"            "readDataEntityNames"          
#> [31] "readDataEntitySize"            "readDataEntitySizes"          
#> [33] "readDataPackage"               "readDataPackageAcl"           
#> [35] "readDataPackageRmd"            "readDataPackageArchive"       
#> [37] "readDataPackageDoi"            "readDataPackageError"         
#> [39] "readDataPackageFromDoi"        "readDataPackageReport"        
#> [41] "readDataPackageReportAcl"      "readDataPackageReportRmd"     
#> [43] "readDataPackageReportChecksum" "readDataPackageReportDoi"     
#> [45] "readEvaluateReport"            "readMetadata"                 
#> [47] "readMetadataDublinCore"        "readMetadataAcl"              
#> [49] "readMetadataRmd"               "readMetadataChecksum"         
#> [51] "readMetadataDoi"               "readMetadataFormat"           
#> [53] "searchDataPackages"            "updateDataPackage"            
#> [55] "createSubscription"            "deleteSubscription"           
#> [57] "executeSubscription"           "getMatchingSubscriptions"     
#> [59] "getSubscriptionWithId"         "notifyOfEvent"                
#> [61] "createJournalCitation"         "deleteJournalCitation"        
#> [63] "getCitationWithId"             "listDataPackageCitations"     
#> [65] "listPrincipalOwnerCitations"  
} # }
```
