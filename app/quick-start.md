# Valence App quick start
This guide will take you through the steps of getting started with Valence App. Deeper documentation can be found throughout this repository, but in this page we'll setup a simple app with a Valence component.
This guide assumes you have already setup a barebones project, but we'll be working with Vite and TypeScript for our example.

## Installation
To get started, let's install `@valence-ui/app` and its sibling packages:
```bash
npm install @valence-ui/app @valence-ui/core @valence-ui/utils
```
`@valence-ui/core` and `@valence-ui/utils` are lower-level packages that supply useful functions to both the `@valence-ui/app` library, and us while developing the app.

## The `ValenceProvider`
Within the root app `.tsx` or `.jsx` file, import and add the `<ValenceProvider>` component, like so:
```tsx
import { ValenceProvider } from '@valence-ui/core'

function App() {
  return ( 
    <>
      <ValenceProvider>
        {/* Your app here */}
      </ValenceProvider>
    </>
  )
}

export default App
```

The `ValenceProvider` provides every component in your app with the styling and default values they require to function correctly. This provider should be wrapped around *every* component in your app, and there should only be a single instance of it. For more information about the `ValenceProvider`, [see this article](../core/valence-provider.md).

Usually, you can go ahead and add some abstraction for routing and page management here, but for now we're going to add some basic Valence components.


## Adding an `AppContainer`
One special layout feature of Valence App is the [`AppContainer`](./layout/app-container.md) component. Within it, we can place a navbar, sidebar and header.

Before we can make any changes, we need to install some more dependencies:
```bash
npm install react-router-dom
```
`react-router-dom` is required because Valence uses the `BrowserRouter` component to navigate between pages. Failing to use this will cause some strange and annoying errors.
```bash
npm install @tabler/icons-react
```
This part is up to you, but Valence prefers the usage of Tabler Icons for its icon library, and even includes some special functions specifically for them.

Now, let's add a bare minimum `<AppContainer>`

```tsx
import { IconBolt, IconCategory, IconUserCircle } from '@tabler/icons-react'
import { AppContainer, Nav } from '@valence-ui/app'
import { Header, Title, ValenceProvider, useDefaultIconProps } from '@valence-ui/core'
import { BrowserRouter } from 'react-router-dom'

function App() {
  const defaultIconProps = useDefaultIconProps();

  return (
    <>
      <ValenceProvider>
        <BrowserRouter>
          <AppContainer
            nav={
              <Nav
                buttons={[
                  {
                    id: "apps",
                    children: <IconCategory {...defaultIconProps.get()} />,
                    highlighted: true,
                    to: "/dashboard",
                  },
                  {
                    id: "account",
                    children: <IconUserCircle {...defaultIconProps.get()} />,
                    to: "/account",
                  },
                  {
                    id: "power",
                    children: <IconBolt {...defaultIconProps.get()} />,
                    to: "/power",
                  }
                ]}
              />
            }
            header={
              <Header>
                <Title>
                  This is a title!
                </Title>
              </Header>
            }
          >

          </AppContainer>
        </BrowserRouter>
      </ValenceProvider>
    </>
  )
}

export default App
```

Now, this is a pretty hefty example to throw at you, so let's break it down.

The `AppContainer` component must have its `nav` and `header` props satisfied to function correctly, so we're supplying the Valence standard `<Nav>` and `<Header>` components here to keep it happy. Technically, you could substitute these components for your own, but to function correctly they must follow some guidelines, which we won't touch on here. 

Then, the `<Nav>` component requires a list of button props supplied in its `buttons` prop. This will help it create the vertical list of icon buttons. Each of these buttons must have an `id` and a `children` component, which is an icon from the Tabler Icons library. 
You may also notice the appearance of the `defaultIconProps.get()` function; this is a special hook and function used to retrieve standardised props for every icon across your app, but must be supplied in this way because of limitations with how Tabler Icons' theming system works.

Finally, we've used the `<Title>` component to create a very basic title in our header. There are many other customisation options available for each component we've presented here, but for now we're going to barrel forward.


## Fixing some visual issues
If you're following along in real-time, you may notice that things are not yet perfect for our app - the entire screen scrolls along the x axis for some reason! To solve this, we're going to introduct a `global.css` file to the mix. 

1. Create a new `global.css` folder wherever you want. In this example, we're going to be doing it in the `src/assets/css/` folder.
2. Add the following snippet to the css file:
```css
body {
  margin: 0;
  width: 100vw;
  height: 100vh;
  overflow-x: hidden;
}

/* Remove ugly blue autofill color from inputs. */
input:-webkit-autofill,
input:-webkit-autofill:hover,
input:-webkit-autofill:focus,
input:-webkit-autofill:active {
  transition: background-color 5000s ease-in-out 0s;
}

/* Fix the scrollbar styling */
*::-webkit-scrollbar {
  width: 10px;
}
*::-webkit-scrollbar-thumb {
  background-color: #11181C20;  
  border-radius: 5px;
}
```

3. Finally, simply import this file at the top of your root app `.tsx` or `.jsx` file, like so:
```tsx
import "./assets/css/global.css"
// the rest of what we wrote before...
```

And our visual issues have disappeared! Next up, fonts!


## Importing & using fonts
To import and use fonts in our app, we are going to need to first place them in our project directory, then reference them in the new `global.css` file, then finally update our `ValenceProvider` to recognise them. 

Firstly, in this example we're going to use [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans), and we're going to place the Bold, BoldItalic, Italic, and Regular variations in the `src/assets/fonts/` folder.

Secondly, we're going to define and import the fonts into our `global.css` file, like so:
```css
@font-face {
  font-family: "PlusJakartaSans";
  src: local("PlusJakartaSans-Regular"), 
       url("../fonts/PlusJakartaSans-Regular.ttf") 
       format("truetype");
  font-weight: 400;
  font-style: normal;
}
@font-face {
  font-family: "PlusJakartaSans";
  src: local("PlusJakartaSans-Italic"), 
       url("../fonts/PlusJakartaSans-Italic.ttf") 
       format("truetype");
  font-weight: 400;
  font-style: italic;
}
@font-face {
  font-family: "PlusJakartaSans";
  src: local("PlusJakartaSans-Bold"),
       url("../fonts/PlusJakartaSans-Bold.ttf") 
       format("truetype");
  font-weight: 800;
  font-style: normal;
}
@font-face {
  font-family: "PlusJakartaSans";
  src: local("PlusJakartaSans-BoldItalic"), 
       url("../fonts/PlusJakartaSans-BoldItalic.ttf") 
       format("truetype");
  font-weight: 800;
  font-style: italic;
}


/* The rest of our css from before */
```
> We're using relative imports here because our fonts are located in a sibling folder to the CSS, but this may differ based upon the location of your files.

Finally, we can head back into our root app file and update the `ValenceProvider` to use our new fonts:

```tsx
function App() {
  // Hooks, etc.

  return (
    <>
      <ValenceProvider
        fontFamily={{
          default: "PlusJakartaSans"
        }}
      >
        {/* BrowserRouter, AppContainer, etc. */}
     </ValenceProvider>
    <>
  )
}
```

And that's it! Plus Jakarta Sans is now being used app-wide. This font will be used for both heading (or `<Title>`) and regular text situations, but will not be used for monospace situations. The `ValenceProvider` provides similar interfaces for heading and monospace fonts, which you can [read about here](../core/valence-provider.md).


## Conclusion
That's about it to this quick start! Valence App is a very extensible componet library, so take a look around this documentation to see how you can use it to its full potential.