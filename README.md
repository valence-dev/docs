Welcome to the documentation for Valence UI, the opinionated design library developed by [Isaac Shea](https://isaacshea.com/).

> **Hey there!** Valence is a project which is in very early stages of its development. This documentation is not updated in-line with the library itself, and fails to mention numerous major changes. You are welcome to use Valence for your own projects, however **I highly advise against this** until at least update 2.0. 
> 
> Version 2.0 will be a ground-up rewrite targeted at fixing many of the shortcomings and hard edges of this library, so stay tuned for that.

## Getting started
Because Valence has been designed to be usable for developing websites, webapps, and native apps, it has been split into three primary package divisions: Web, App and Native, respectively. Each division differs in features and implementations dramatically, so knowing which one you will use before starting is reasonably important. 

### Valence App
[**Get started**](./app/quick-start.md) | `@valence-ui/app` is currently the only available division, and includes components designed specifically for webapps. 

### Valence Web (coming soon)
`@valence-ui/web` will be a division that will provide elements for websites, such as horizontal nav bars, page sections, etc. While it is not strictly incompatible with Valence App, it will contain some elements named the same as it's peer, but implemented very differently (such as the `<Nav>` element).

### Valence Native (coming soon)
Specifically designed for React Native, Valence Native will be a re-implementation of the entire Valence App library using elements from React Native. It will focus on keeping as much of its high-level interface as close to Valence App as possible.

### Other packages
- [**Valence Core**](./core/README.md) - This package includes components and hooks used across both the App and Web divisions of Valence.
- [**Valence Utils**](./utils/README.md) - Miscellaneous low-level features and types used across all packages.
 

## Motivation
This library was developed because I (Isaac Shea) saw a need to build my own library to suit my own needs. I was previously using [Mantine](https://mantine.dev/), but ended up constructing an entire library of components *on-top* of Mantine to re-style and re-implement components that didn't suit my self-imposed design requirements. Valence is my solution to that, and has been designed to be very opinionated towards the design style I aim for in each project. I don't see this library being of particular use to people who want low-level control over their components, however it may be handy for those looking for a lightweight and pre-styled library that works well enough for them.

This project will likely receive updates as I find and fix bugs, develop features and generally use the library for my own projects, but is open source so that any other people who want to use or help develop it can do so!