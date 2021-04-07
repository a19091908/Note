# HTTP Session and Cookies
1. Cookies
    * some of data is stored in the cookies such as sessionid, userName, and user's perferences......
    * the cookies are stored in the client side 
    * Two types of cookies:
        1. Session cookies: 
            deleted when the current session ends.  
        2. Permanent cookies: 
            deleted at a date specified by the Expires attribute, or after a period of time specified by the Max-Age attribute.
    * **Set-Cookie** attributes:
        1. HttpOnly
            document.cookie can get the cookie except setting Set-Cookie with HttpOnly.
        2. Domain
            allowed to recieve cookies on the domain and its subdomain. If not specified, only your website domain will recieve the cookies. 
        3. Path
            indicates which paths of your website to which the cookies are able to send
        4. SameSite
            1. Lax (default)
                Cookies are not sent on normal cross-site subrequests (for example to load images or frames into a third party site), but are sent when a user is navigating to the origin site (i.e. when following a link).
            2. Strict
                Cookies will only be sent in a first-party context and not be sent along with requests initiated by third party websites.
            3. none
2. Session
    * it is stored in the server side
    * the session id stored in the cookie could indicate your session in the server

<hr>
Ref:
https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies