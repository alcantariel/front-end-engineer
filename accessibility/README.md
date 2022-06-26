# Accessibility

Accessibility means to make users able to use web applications even with some disability. The content needs to be accessible as possible, no matter an individual's physical and cognitive abilities and how they access the web.

"The Web is fundamentally designed to work for all people, whatever their hardware, software, language, location, or ability. When the Web meets this goal, it is accessible to people with a diverse range of hearing, movement, sight, and cognitive ability." (W3C - Accessibility)

There are some characteristics of an accessible application:

- [Semantics in HTML](../html/README.md#semantics)
- Semantics in CSS
- Semantics in JavaScript

<br>

## Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA)

Is a specification written by the W3C, it includes a set of [HTML attributes](../html/README.md#attributes) to provide additional semantics and improve accessibility.

There are three main features, [Roles](#roles), [Properties](#properties) and [States](#states). These features, when set does not affect anything in the web page structure, DOM, etc... Although these attributes can be useful for selecting elements by CSS.

These attributes affect only the information exposed by the browser's accessibility API (where screenreaders get their information from).

<br>

### Roles

Defines what an element is or does. Many of these are called landmark roles and give more semantics to HTML elements, even if the element is correct, such as `<nav role="navigation">`.

<br>

### Properties

Can be used to give them extra meaning or semantics. As an example, `aria-required="true"` specifies that a form input needs to be filled in order to be valid.

<br>

### States

Define the current conditions of elements, such as `aria-disabled="true"`, which specifies to a screenreader that the form input is currently disabled.

States differ from properties in that properties don't change throughout the lifecycle of an app.

<br>

## Accessibility Multimedia

<br>

## Mobile Accessibility

<br>

## References

- [Web Accessibility Initiative (WAI)](https://www.w3.org/WAI/)
- [Accessibility | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- [WAI-ARIA basics](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/WAI-ARIA_basics)
