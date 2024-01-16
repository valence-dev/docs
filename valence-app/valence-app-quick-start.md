# 📱 Valence App quick start

> **Compatibility note:** Valence App is incompatible with other Discipline packages in the Valence library. For more information about this, see the [Getting Started page](../overview/getting-started.md#about-the-discipline-packages).

Valence App is a Disciplinary package in the Valence library the contains a collection of components designed specifically for web and mobile applications.&#x20;

## Installation

To get started, install `@valence-ui/app` and the [Core packages](../overview/getting-started.md#about-the-core-packages), like so:

```bash
npm install @valence-ui/app @valence-ui/core @valence-ui/utils
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
