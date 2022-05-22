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

An example of a cross-origin request is, the front-end JavaScript served at `https://domain-a.com` uses XMLHttpRequest to request for `https://domain-b.com/data.json`.

For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts, following the same-origin policy. This means that a web application using those APIs can only request resources from the same origin unless the response from other origins includes the right CORS headers.

<br>

## Clickjacking

Is when an attacker uses multiple transparent layers over the current page and when the user interacts with any element on the page, he actually will be interacting with the transparent layer, which will redirect to another page.

This new page is a clone of another one, with a similar domain name and everything to pass the impression that the user is interacting with the secure page.

This new page is owned by the attacker, so you will be interacting with this page, entering all your confidential information and sending it to the attacker.

Common ways for preventing:

- Adding the [Content Security Policy](#content-security-policy) response header that will prevent embedding your site from other domains.
- Properly configured [Cookies](../cookie/README.md#cookie), with the flag [SameSite](../cookie/README.md#samesite) equals to Strict or Lax.

<br>

## Cross-Site Scripting (XSS)

Is an attack that is a type of injection, which injects malicious scripts into trusted websites.

It occurs when a website "allows" an attacker to inject into the website malicious client-side code.

With this injection, the end-user has no way to know that the script is malicious, and will execute the script because it thinks the script came from a trusted source. The malicious script can access any cookies, session tokens, or other sensitive information retained by the browser and used with that site.

Imagine a blog that allows input comments, but in this comment, an attacker can insert any script or tag, and these malicious comments can be read and clicked by the other users. Now you can see the hijacking.

Common ways for preventing:

- Don't set important tokens at [Local Storage](../web-storage-api/README.md#local-storage), it's vulnerable to this type of attack.
- Don't set important tokens as query params or request bodies, attackers can be sniffing or intercepting these requests with these exposed tokens.
- Use [Cookie](../cookie/README.md#cookie) with [HttpOnly](../cookie/README.md#httponly) flag.

<br>

## Cross-Site Request Forgery (CSRF)

Is an attack that forces an end-user to execute unwanted actions on a web application in which they’re currently logged in.

Is conducted using malicious social engineering, such as an email or link that tricks the victim into sending a forged request to a server.

A successful attack can force the user to perform state-changing requests like transferring funds, changing their email address, and so forth. But it's limited by the user's privileges.

Common ways for preventing:

- [Synchronizer Token Pattern](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html#synchronizer-token-pattern).

<br>

## Distributed Denial of Service (DDoS)

Is an attack focused on making a resource (site, application, server) unavailable for the purpose it was designed.

Normally occurs using bots, attacking high-profile servers like banks or payment gateways. DDoS concerns computer networks and CPU resource management.

If a service receives a very large number of requests, it may cease to be available to legitimate users. In the same way, a service may stop if a programming vulnerability is exploited, or the way the service handles the resources it uses.

This type of attack can significantly degrade the service quality experienced by legitimate users. These attacks introduce large response delays, excessive losses, and service interruptions, resulting in a direct impact on availability.

<br>

## SQL Injection

Is an attack that consists of taking advantage of applications that fail to validate user input.

Hackers can maliciously pass SQL commands through the input inside the application for execution by the application database. A successful attack can read, modify and delete sensitive data from the database.

Common ways for preventing:

- Sanitize input values.

<br>

## Unrestricted File Upload

Is an attack that represents a significant risk to applications. The first step in many attacks is to get some code to the system to be attacked. Then the attack only needs to find a way to get the code executed. Using a file upload helps the attacker accomplish the first step.

Common ways for preventing:

- The list of permitted extensions should be reviewed as it can contain malicious extensions as well.

<br>

## References

- [OWASP](https://owasp.org/)
- [MDN Web Docs | HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
- [Imperva](https://www.imperva.com/learn/application-security)
- [10 Dicas de Segurança para Projetos Front End](https://dev.to/felipperegazio/10-dicas-de-seguranca-para-projetos-front-end-2385)
