---
description: 'Last updated: 2.0.0 (16/01/2024)'
---

# 🏄♂ Getting started

Valence is designed to be usable across numerous development disciplines, including websites, web-apps, and native applications (via something like Capacitor.JS). These specific use-cases inform Valence's Discipline packages, which are effectively its core.

## About the Core packages

Valence's two core packages, `core` and `utils`, are required for all projects that use Valence. They provide essential components and utility types, and can then be expanded upon by Discipline packages. If no Discipline package exists to serve your use case, you can take the Core packages and develop your own expansions.

## About the Discipline packages

Discipline packages are optional expansions to the Core packages that provide utility for specific use-cases. Oftentimes, these packages are not compatible, and may use the same names for very different components. As such, it is important to decide which Discipline package you will use before starting your project.

> While it is recommended to use one Discipline package in your project, you can just use the Core packages, then build out your own Discipline package/s for your own use case.

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h4>Valence App</h4></td><td>Components and UI patterns designed specifically for webapp and native app environments.</td><td></td><td><a href="broken-reference">Broken link</a></td></tr><tr><td></td><td><h4>Valence Web</h4></td><td><em>(coming soon)</em></td><td></td></tr></tbody></table>

## About the Plugin packages

Plugin packages are the third level of Valence packages, and are completely optional. They provide specific and sometimes niche utilities and components, and are designed to be compatible with all Discipline packages, unless otherwise specified.

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h4>Valence Carousel</h4></td><td>A custom horizontal carousel component designed for maximum usability in desktop and mobile environments.</td><td></td><td><a href="../valence-plugins/valence-carousel/">valence-carousel</a></td></tr></tbody></table>
