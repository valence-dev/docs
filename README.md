# Valence documentation
Welcome to the documentation for Valence! Valence is an opinionated React component library [I (Isaac Shea)](https://isaacshea.com/) designed with the primary intention of using it in my web development projects. It is heavily inspired by [Mantine](https://mantine.dev/) and features a very similar development workflow. **Currently, Valence is in very early stages of its development**, thus it is not recommended for production use for anybody else. I have however decided to make it open source as I feel something like this benefits greatly from the opinions of multiple individuals.


## Getting started
(Coming soon). Currently, the package is not yet available on NPM, and cannot be easily setup. Once [v1.0](https://github.com/orgs/valence-dev/projects/1) has released, this section will be updated with setup instructions and best practices.


## Divisions
Valence is split into five major divisions, each of which serving their own purpose:
1. [**Utils:**](./utils/README.md) underlying infrastructure that all four other divisions rely on
2. [**Core:**](./core/README.md) basic components designed to be used across both websites, webapps, and native apps
3. [**App:**](./app/README.md) components specifically designed for use within webapps
4. **Web:**  components specifically design for use on websites (coming soon) 
5. **Native:** a re-implementation of the entire library in React Native (coming soon)

The App and Web libraries both rely on the Utils and Core libraries, but are incompatible with one another because they may contain double-ups that change dramatically (the `<Nav>` component is one such example).

The Native library contains completely new implementations of the Utils and Core libraries built from the ground up for React Native, and for obvious reasons is incompatible with the other four libraries. Valence Native is designed to keep as much of its high-level interface identical to the web version, for continuity's sake.


## Core concepts
### Mobile/desktop inter-operability
Valence has developed a [breakpoint ecosystem](./utils/breakpoints.md) that allows components to seamlessly switch layout based upon the size class of the device on which the site is operating. This allows for a smooth developer experience when designing and constructing applications and websites. To avoid control being stripped from you as a developer, many of the foundational components upon which automated ones are constructed are exposed for your own modification and re-implementation.

### Light & dark scheme switching
Valence somewhat forcibly requires every site to switch between light and dark schemes in tandem with the system theme. This means that users will always have the most comfortable viewing experience on your application or site, and is implemented via a robust [color system](./core/colors.md) and [context provider](./core/valence-provider.md). 

### Polymorphic components
Many Valence components are designed with [polymorphism](./utils/polymorphism.md) in mind, allowing you to develop powerful and versatile components, buttons and layout elements.