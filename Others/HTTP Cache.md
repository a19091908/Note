# HTTP Cache
### Freshness
    1. Expires
    It indicates the expire date.
    Ex: 
    Expires: Wed, 21 Oct 2017 07:28:00 GMT
    2. max-age
    It indicates the resource will expire after certain **seconds**. 
    Ex:
    Cache-Control: max-age=30
    #### Note that if a response includes both Expires and max-age, the max-age overrides the Expires value
### Is modified
    If the resource is not fresh, it will validate whether the resource is modified. If modified, it will not download the new resource, else it will use the same resource in your browser.
#### The validation process includes: 
    1. Last-Modified & If-Modified-Since
        Last-Modified records the last modified date of the file. If the resource is not fresh, the request of the resource will include If-Modified-Since: [Last-Modified] for checking the resouce is modified on the server side.
    2. Etag & If-None-Match
        Etag is like a hash value of the content of the file. If the resource is not fresh, the request of the resource will include If-None-Match: [Etag] for checking the resouce is modified on the server side.