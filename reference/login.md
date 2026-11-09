# Login to the EDI repository

Login to the EDI repository

## Usage

``` r
login(userId = NULL, userPass = NULL, key = NULL, config = NULL)
```

## Arguments

- userId:

  (character) User identifier of an EDI data repository account.

- userPass:

  (character) Password of `userId`

- key:

  (character) EDI-API access key.

- config:

  (character) Path to config.txt, which contains `userId` and `userPass`
  or `key` (see details below)

## Value

(NULL) No return value. The token or API key is written to its
respective environment variable.

## Details

If `userId`, `userPass`, `key`, and `config` are NULL, the console will
prompt for credentials.

`config`: Supplying credentials in a file named config.txt facilitates
authentication within automated/unassisted processes. Contents of this
file should be new line separated and have the form "\<argument\> =
\<value\>" (e.g. userId = myname or key = my_api_key).

## Note

Legacy credentials login only works when authenticating with EDI
credentials. For modern token-free authentication, generate an API key
from the EDI Portal and supply it as the `key` parameter or in your
`config` file.

Be careful not to accidentally share your credentials. Some tips to
avoid this:

- Don't write code that explicitly lists your credentials.

- Don't save your workspace when exiting an R session.

- Do store your credentials as environmental variables and reference
  these.

- Do use `config` but if using version control ensure the config.txt
  file is listed in your .gitignore.

If you may have shared your credentials, please reset your password at
<https://dashboard.edirepository.org/dashboard/auth/reset_password_init>.

## See also

Other Authentication:
[`logout()`](https://docs.ropensci.org/EDIutils/reference/logout.md)

## Examples

``` r
if (FALSE) { # \dontrun{

# Interactively at the console
login()
#> EDI-API key (leave blank to use username/password): "my_api_key"

# Programmatically with an API key
login(key = "my_api_key")

# Programmatically with legacy function arguments
login(userId = "my_name", userPass = "my_secret")

# Programmatically with a file containing credentials
login(config = paste0(tempdir(), "/config.txt"))
} # }
```
