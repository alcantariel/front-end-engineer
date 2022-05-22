# Web Storage API

This browser API provides mechanisms that can store pairs of keys and values and is more intuitive than using [Cookies](../cookie/README.md#cookie).

<br>

## Local Storage

Maintains a separate storage area for each origin.

It will persist data even if you close the page (tab) or browser.

This persisted data has no expiration date, which means that the stored data only can be cleared through JavaScript, clearing the browser cache or clearing directly
at the Application tab inside the DevTools.

Has a limit of data size up to 5mb.

<br>

## Session Storage

Maintains a separate storage area for each origin.

It will be available for the duration of the page session (including page reloads).

It means that the stored data is only available until the page (tab) or browser is closed.

Has a limit of data size up to 5mb.

<br>

## Usage

Both are available via `Window.localStorage` and `Window.sessionStorage` properties.

To be more precise, in supporting browsers the Window object implements the WindowLocalStorage and WindowSessionStorage objects, which are the localStorage and sessionStorage properties. Invoking one of these will create an instance of the Storage object, through which data items can be set, retrieved and removed.

<br>

## What can I store inside Local Storage and Session Storage?

Both are vulnerable to [XSS](../security/README.md#cross-site-scripting-xss) attacks, so Local Storage and Session Storage are good places to store public and non-sensitive data.

<br>

## References

- [Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API)
- [10 Dicas de Segurança para Projetos Front End](https://dev.to/felipperegazio/10-dicas-de-seguranca-para-projetos-front-end-2385)
