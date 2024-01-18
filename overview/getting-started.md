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

<details>

<summary>Valence App</summary>

Valence App is currently the only Discipline package available, and includes components designed specifically for web and native apps.

[valence-app-quick-start.md](../valence-app/valence-app-quick-start.md "mention")

</details>

<details>

<summary>Valence Web</summary>

Valence Web is a theoretical second Discipline package, and would include components specifically designed for website environments.

</details>

## About the Plugin packages

Plugin packages are the third level of Valence packages, and are completely optional. They provide specific and sometimes niche utilities and components, and are designed to be compatible with all Discipline packages, unless otherwise specified.
