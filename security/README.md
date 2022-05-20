# Security

As front-end engineers, we should keep in mind that security is not exclusive responsibility for the back-end or infrastructure.

There are malicious attacks started on the front-end and we will discuss some of these and how to prevent them too.

## Open Web Application Security Project (OWASP)

Is a non-profit foundation that works to improve software security. Through community-led open-source projects, is the source for developers to secure the web.

<br>

## Headers

Describes HTTP response headers that increase application security. Once set, these response headers will work together with the browser and help him with the vulnerabilities.

### X-Frame-Options

Improves protection against [Clickjacking](#clickjacking).

Tells the browser if it is allowed to embed the page inside another website inside via iframe or something like.

<br>

### HTTP Strict Transport Security

Helps to protect websites against protocol downgrade attacks and cookie hijacking.

It allows web servers to declare that browsers should only interact using HTTPS connections.

<br>

### Content Security Policy

If enabled, CSP has significant impact on the way browsers render pages (e.g., inline JavaScript is disabled by default and must be explicitly allowed in the policy).

Helps to detect and mitigate certain types of attacks, including [Cross-Site Scripting (XSS)](#cross-site-scripting-xss) and data injection attacks. These attacks are used for everything from data theft, to site defacement, to malware distribution.

<br>

### Clear-Site-Data

Clears browsing data (cookies, storage, cache) associated with the requesting website.

This header is useful for example, during a logout process, in order to ensure that all stored content on the client side like cookies, storage and cache are removed.

<br>

## Clickjacking

<br>

## Cross-Origin Resource Sharing (CORS)

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
