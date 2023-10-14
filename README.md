# Valence documentation
Welcome to the documentation for Valence! Valence is an opinionated React component library [I (Isaac Shea)](https://isaacshea.com/) designed with the primary intention of using it in my web development projects. It is heavily inspired by [Mantine](https://mantine.dev/) and features a very similar development workflow. **Currently, Valence is in very early stages of its development**, thus it is not recommended for production use for anybody else. I have however decided to make it open source as I feel something like this benefits greatly from the opinions of multiple individuals.


## Divisions
Valence is split into three high-level packages, with two supporting packages that provide common and lower-level functions. These high-level packages will be referred to as *divisions*. The three divisions are incompatible with one another, so you must choose during installation which one you want to use.

### 1. Valence App
`@valence-ui/app` is currently the only publicly-available division, and includes components designed specifically for webapps. [Avant by Isaac Shea](https://avant.isaacshea.com/) is made with Valence App.

**Get started:** [read the guide](./app/quick-start.md)


### 2. Valence Web (coming soon)
`@valence-ui/web` will be the second Valence division, and will support common website design patterns.


### 3. Valence Native (coming soon)
`@valence-ui/native` will be the third Valence divison, and will include a ground-up rewrite of the entire library specifically for React Native. Valence Native is designed to keep as much of its high-level interface identical to the web version, for continuity's sake.


### Other packages
- [**Valence Core**](./core/README.md) - This package includes components and hooks used across both the App and Web divisions of Valence.
- [**Valence Utils**](./utils/README.md) - Miscellaneous low-level features and types used across all packages.


## Reading these docs
This documention is best viewed with the Storybook instance alongside it. These docs do not contain any imagery, thus having a live preview of all elements is a valuable addition until a proper website for documentation is developed. To run the Storybook instance:
1. Download the relevant Valence repositories from GitHub
2. Run `npm install` to install all required dependencies
3. Run `npm run storybook` and open `localhost:6006` to view the preview


## Core concepts
### Mobile/desktop inter-operability
Valence has developed a [breakpoint ecosystem](./utils/breakpoints.md) that allows components to seamlessly switch layout based upon the size class of the device on which the site is operating. This allows for a smooth developer experience when designing and constructing applications and websites. To avoid control being stripped from you as a developer, many of the foundational components upon which automated ones are constructed are exposed for your own modification and re-implementation.

### Light & dark scheme switching
Valence somewhat forcibly requires every site to switch between light and dark schemes in tandem with the system theme. This means that users will always have the most comfortable viewing experience on your application or site, and is implemented via a robust [color system](./core/colors.md) and [context provider](./core/valence-provider.md). 

### Polymorphic components
Many Valence components are designed with [polymorphism](./utils/polymorphism.md) in mind, allowing you to develop powerful and versatile components, buttons and layout elements.