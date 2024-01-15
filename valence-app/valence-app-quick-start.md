# 📱 Getting started

> **Compatibility note:** Valence App is incompatible with other Discipline packages in the Valence library. For more information about this, see the [Getting Started page](../overview/getting-started.md#about-the-discipline-packages).

Valence App is a Disciplinary package in the Valence library the contains a collection of components designed specifically for web and mobile applications.&#x20;

## Installation

To get started, install `@valence-ui/app` and the [Core packages](../overview/getting-started.md#about-the-core-packages), like so:

```bash
npm install @valence-ui/app @valence-ui/core @valence-ui/utils
```

## Adding a global CSS file

For Valence to function correctly, a global CSS file needs to be created to clean up visual issues that are created by default styling from browsers.&#x20;

1. Create a new `global.css` file in your assets director. In this example, we'll save it in `src/assets/css`.&#x20;
2. Copy and add the following snipped to the file:

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

3. Finally, import this file at the top of the root app file (usually `App.tsx` or `App.jsx`):

```tsx
import "./assets/css/global.css"
// Other code...
```



## Adding the `ValenceProvider`

The `ValenceProvider` provides every component in your app with the relevant styling and default values that they require to function correctly.

Within the root app file (usually `App.tsx` or `App.jsx`), import and add the `ValenceProvider`:

```tsx
import { ValenceProvider } from "@valence-ui/core"

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

That's all there is to it! From here, you can start to build out your application.
