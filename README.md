# Goldfish

## Sample requests

### GET /findings/_design/by_host/_view/by_host?key="hostname123"

Will return a json array of all findings to a given hostname.
By appending "&include_docs=true" it will also contain the whole entry

### POST finding

