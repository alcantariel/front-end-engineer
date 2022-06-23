# Hypertext Markup Language (HTML)

Is a markup language that tells the browsers how to structure the web pages.

It consists of a series of tags or elements, which you use to enclose, wrap, or mark up different parts of content to make it appear or act in a certain way.

<br>

## Anatomy of an HTML Element

```html
<p>Drink water</p>
```

- The opening tag `<p>` consists of the name of the element, wrapped in opening and closing angle brackets. This opening tag marks where the element begins.
- The content `Drink water` is the content of the element.
- The closing tag `</p>` is the same as the opening tag, except that it includes a forward slash `/` before the element name. This marks where the element ends.

<br>

## Block versus Inline Elements

There are two important categories of elements to know in HTML: block-level elements and inline elements.

### Block

Block-level elements form a visible block on a page. A block-level element appears on a new line following the content that precedes it. Any content that follows a block-level element also appears on a new line.

A block-level element might represent headings, paragraphs, lists, navigation menus or footers.

### Inline

Inline elements are contained within block-level elements and surround only small parts of the document's content.

An inline element will not cause a new line to appear in the document. It is typically used with text, for example, an `<a>` element creates a hyperlink, and elements such as `<em>` or `<strong>` create emphasis on the same line/hyperlink.

<br>

## Empty elements

Not all elements have a closing tag. Some elements consist of a single tag, which is typically used to insert/embed something in the document.

For example, the `<img>` element embeds an image file onto a page:

```html
<img src="https://i.kym-cdn.com/photos/images/original/001/995/324/a4a.jpg" />
```

<br>

## Attributes

Elements can also have attributes. They are inside the opening tag and look like the `src` inside the `<img>` tag above.

Attributes contain extra information about the element that won't appear in the content. In this case, indicates what's the URL of the image will be loaded.

An attribute should have:

- A space between it and the element name;
- The attribute name is followed by an equal sign;
- A value, wrapped with quote marks;
- Boolean attributes are written without value, only attribute name.

<br>

## Anatomy of an HTML document

Individual HTML elements aren't very useful on their own. This example will combine elements to form an entire HTML page:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Title of my page</title>
  </head>
  <body>
    <p>This is my page</p>
  </body>
</html>
```

- `<!DOCTYPE html>` act as a link to a set of rules that the HTML page had to follow to be considered good HTML.
- `<html>` element wraps all the content on the page. It's the root element.
- `<head>` element act as a container for everything you want to include on the HTML page. This includes keywords and a page description that would appear in search results, CSS to style, and more...
- `<meta charset="utf-8">` represents metadata that cannot be represented by other HTML meta-related elements, like `<base>`, `<link>`, `<script>`, `<style>` or `<title>`. The charset attributes set the character set for your document to UTF-8, which includes most characters from the vast majority of human written languages. With this setting, the page can now handle any textual content it might contain. There is no reason not to set this, and it can help avoid some problems later.
- `<title>` sets the title of the page, which is the title that appears in the browser tab the page is loaded in.
- `<body>` contains all the content that displays on the page, including text, images, videos, games, playable audio tracks, or whatever else.

<br>

## Semantics

It refers to giving meaning to a piece of code, like "what purpose or role does that HTML element has?", rather than "how does this div look like?".

<br>

## References

- [Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)
- [HTML: A good basis for accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)
- [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)
