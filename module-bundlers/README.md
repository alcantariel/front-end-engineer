# Module Bundlers

A module bundler is a tool that takes parts of JavaScript and its dependencies and bundle these parts into a single static file.

It starts with an input file and from there it bundles all the code needed for that input file.

There are two main stages of a bundler:

- Dependency resolution: starting from an entry point "index.js", the goal of dependency resolution is to look for all your code's dependencies (other pieces of code it needs to work as their imports) and build a graph called a dependency graph.
- Packaging: once dependency resolution is done, it compress or convert your dependency graph into a single file that the application can use.

## webpack
