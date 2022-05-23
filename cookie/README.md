# Cookie

It's a small piece of data left on the user's computer via browsers.

Are used to personalize a user's web experience. It may contain the user's preferences when accessing that website.

Can be set, modified and deleted at the server level using the `Set-Cookie HTTP Header` or with `JavaScript via document.cookie`.

<br>

## Attributes

Defines the cookie name and its value. A cookie definition begins with a name-value pair.

`<cookie-name>=<cookie-value>`.

<br>

### Expires=\<date\>

Indicates the maximum lifetime of the cookie as an HTTP-date timestamp.

If unspecified, the cookie becomes a session cookie. A session finishes when the client shuts down, after which the session cookie is removed.

When an Expires date is set, the deadline is relative to the client, not the server.

<br>

### Max-\Age=<number\>

Indicates the number of seconds until the cookie expires. A zero or negative number will expire the cookie immediately.

If Expires and Max-Age are set, Max-Age has precedence.

<br>

### Domain=\<domain-value\>

Defines the host to which the cookie will be sent.

If omitted, the default domain is the host of the current document URL, not including subdomains.

Multiple domain values are not allowed, but if a domain is specified, then subdomains are always included.

<br>

### Path=\<path-value\>

Indicates the path that must exist in the requested URL for the browser to send the Cookie header.

The forward slash (/) character is interpreted as a directory separator, and subdirectories are matched as well.

For example:

`Path=/docs`

- the request paths /docs, /docs/, /docs/Web/, and /docs/Web/HTTP will all match.
- the request paths /, /docsets, /fr/docs will not match.

<br>

### Secure

Indicates that the cookie is sent to the server only when a request is made with `https`.

Do not assume that Secure prevents all access to sensitive information in cookies.

Cookies with this attribute can still be read or modified either with access to the client's hard disk or from JavaScript if the [HttpOnly](#httponly) cookie attribute is not set.

<br>

### HttpOnly

Forbids JavaScript from accessing the cookie, for example, through the `Document.cookie` property.

A cookie that has been created with HttpOnly will still be sent on requests, but this mitigates attacks against [XSS](../security/README.md#cross-site-scripting-xss).

<br>

### SameSite=\<samesite-value\>

Controls whether or not a cookie is sent with cross-origin requests, providing some protection against [CSRF](../security/README.md#cross-site-request-forgery-csrf).

<br>

#### Strict

It means that the browser sends the cookie only for same-site requests, that is, requests originating from the same site that set the cookie.

If a request originates from a URL different from the current one, no cookies with the SameSite=Strict attribute are sent.

<br>

#### Lax

It means that the cookie is not sent on cross-site requests, such as on requests to load images, but is sent when a user is navigating to the origin site from an external site.

This is the default behavior if the SameSite attribute is not specified.

#### None

It means that the browser sends the cookie with both cross-site and same-site requests.

The [Secure](#secure) attribute must also be set when setting this value, like so `SameSite=None; Secure`.

<br>

## References

- [MDN Web Docs | Cookie](https://developer.mozilla.org/en-US/docs/Glossary/Cookie)
- [MDN Web Docs | Set-Cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie)
- [What are Cookies?](https://www.kaspersky.com/resource-center/definitions/cookies)
