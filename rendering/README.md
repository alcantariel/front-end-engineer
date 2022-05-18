# Rendering

As developers, we often came across decisions that affect the entire architecture of our applications.

One of the main decisions is what kind of rendering we will need to use.

Rendering has some attributes called Web Vitals that are important measures and that should be part of the decision according to the web page will be rendered and business necessities.

<br>

## Web Vitals

Web Vitals is an initiative by Google to provide quality signals that are essential to delivering a great user experience on the web.

Google provides many tools to measure and report on performance.

The Web Vitals initiative aims to simplify the landscape and help sites focus on the metrics that matter most.

<br>

### Largest Contentful Paint (LCP)

Reports the render time of the largest image or text block visible, relative to when the page first started loading.

It's about rendering all the page content.

LCP is related to [FCP](#first-contentful-paint-fcp).

<br>

### First Input Delay (FID)

Measures the time of the user's first interaction with the page (i.e. when they click a link, tap on a button, or use a custom JavaScript-powered control) to the time when the browser can begin processing event handlers in response to that interaction.

<br>

### Cumulative Layout Shift (CLS)

It's a measure related to unexpected changes in the layout of the rendered page.

It usually happens when some async resource is loaded, and consequently adds elements in the DOM, causing the layout to move, resulting in a high [CLS](#cumulative-layout-shift-cls) and a strange user experience.

<br>

### Time to First Byte (TTFB)

It's a measure of the time between the request for a resource and when the first byte of response begins to arrive.

Reducing latency in connection setup time, and on the backend will contribute to a lower [TTFB](#time-to-first-byte-ttfb).

<br>

### First Contentful Paint (FCP)

It's a measure of the time from when the page starts loading to when any part of the page's content is rendered on the screen.

It's about rendering some content on the page, even if not fully loaded. Is related to [LCP](#largest-contentful-paint-lcp).

<br>

### Time to Interactive (TTI)

It's a measure of the time from when the page starts loading to when its main sub-resources have loaded and it is capable of reliably responding to user input quickly.

<br>

### Total Blocking Time (TBT)

It's a measure of the total amount of time between [FCP](#first-contentful-paint-fcp) and [TTI](#time-to-interactive-tti) where the main thread was blocked for long enough to prevent input responsiveness.

<br>

## Kinds of Rendering

### Client-Side Rendering (CSR)

It means rendering web pages directly in the browser. The entire bundle is downloaded when the user opens the application.

The main disadvantage of this approach is that the bundle size to be downloaded grows as the application evolves, increasing the initial load time or a higher [FCP](#first-contentful-paint-fcp).

<br>

### Server-Side Rendering (SSR)

Renders all the requested HTML content on the server. This will avoid requests to get some extra data on the client-side, as it is handled before the browser gets a response from the request.

Server-side rendering generally produces fast [FCP](#first-contentful-paint-fcp). The page rendering on the server makes it possible to avoid sending too much JavaScript to the client, which helps to achieve fast [TTI](#time-to-interactive-tti) too.

The main disadvantage of this approach is the server page generation, it takes time, which can result in a slower [TTFB](#time-to-first-byte-ttfb).

<br>

### Static Site Generator (SSG)

Static rendering happens at application build time and offers fast [FCP](#first-contentful-paint-fcp), [TTI](#time-to-interactive-tti) and better [TTFB](#time-to-first-byte-ttfb) than server-side rendering, as static is not generated at request time.

This is to generate a file or HTML for each route in advance.

The main disadvantage of this approach is that files HTML are generated for each URL available in the application and this can become impracticable when it's not possible to predict these URLs in advance.

<br>

## References

- [Web Vitals](https://web.dev/vitals/)
- [Rendering on the Web](https://web.dev/rendering-on-the-web/)
- [Measuring performance](https://nextjs.org/docs/advanced-features/measuring-performance)
