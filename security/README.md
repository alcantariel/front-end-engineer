# Security

As front-end engineers, we should keep in mind that security is not exclusive responsibility for the back-end or infrastructure.

There are malicious attacks started on the front-end and we will discuss some of these and how to prevent them too.

<br>

## Open Web Application Security Project (OWASP)

Is a non-profit foundation that works to improve software security. Through community-led open-source projects, is the source for developers to secure the web.

<br>

## HTTP Headers

Describes HTTP response headers that increase application security. Once set, these response headers will work together with the browser and help him with the vulnerabilities.

<br>

### X-Frame-Options

Improves protection against [Clickjacking](#clickjacking).

Tells the browser if it is allowed to embed the page inside another website inside via iframe or something like that.

<br>

### HTTP Strict Transport Security

Helps to protect websites against protocol downgrade attacks and cookie hijacking.

It allows web servers to declare that browsers should only interact using HTTPS connections.

<br>

### Content Security Policy

If enabled, CSP has a significant impact on the way browsers render pages (e.g., inline JavaScript is disabled by default and must be explicitly allowed in the policy).

Helps to detect and mitigate certain types of attacks, including [Cross-Site Scripting (XSS)](#cross-site-scripting-xss) and data injection attacks. These attacks are used for everything from data theft, to site defacement, to malware distribution.

<br>

### Clear-Site-Data

Clears browsing data (cookies, storage, cache) associated with the requesting website.

This header is useful for example, during a logout process, to ensure that all stored content on the client-side like cookies, storage and cache is removed.

<br>

## Cross-Origin Resource Sharing (CORS)

Allows a server to indicate which origins will be able to loading resources inside the browser. It has a mechanism by which browsers make a "preflight" request to the server hosting the cross-origin resource, to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.

An example of a cross-origin request is, the front-end JavaScript served at https://domain-a.com uses XMLHttpRequest to request for https://domain-b.com/data.json.

For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts, following the same-origin policy. This means that a web application using those APIs can only request resources from the same origin unless the response from other origins includes the right CORS headers.

<br>

## Clickjacking

Is when an attacker uses multiple transparent layers over the current page and when the user interacts with any element on the page, he actually will be interacting with the transparent layer, which will redirect to another page.

This new page is a clone of another one, with a similar domain name and everything to pass the impression that the user is interacting with the secure page.

This new page is owned by the attacker, so you will be interacting with this page, entering all your confidential information and sending it to the attacker.

Common ways for preventing:

- Adding the [Content Security Policy](#content-security-policy) response header that will prevent embedding your site from other domains.
- Properly configured [Cookies](../localstorage-sessionstorage-cookies/README.md#cookies), with the flag SameSite equals to Strict or Lax.

<br>

## Cross-Site Scripting (XSS)

<br>

## Cross-Site Request Forgery (CSRF)

<br>

## Distributed Denial of Service (DDoS)

<br>

## SQL Injection

<br>

## Unrestricted File Upload

<br>

## References

- [OWASP](https://owasp.org/)
- [MDN Web Docs | HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
