---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# App Container

{% hint style="warning" %}
This component has changed dramatically in Valence 3! [View the update notes](../../../update-notes/3.0.0.md).
{% endhint %}

The `AppContainer` is an all-in-one component that creates a container in which the content of the app resides. It is designed to adapt responsively across all device classes to provide a consistent yet tailored experience.

## Usage

```tsx
import { AppContainer, AppNav, Button, Header } from "@valence-ui/core";
import { BrowserRouter } from "react-router-dom";
import { IconCategory } from "@tabler/icons-react";

export default function App() { 
    return ( 
        <BrowserRouter>
            <ValenceProvider>
                <AppContainer
                    nav={
                        <AppNav
                            buttons={[
                                {
                                    id: "page1",
                                    children: <IconCategory />,
                                    highlighted: true,
                                    to: "/home",
                                },
                                // More buttons...
                            ]}
                        />
                    }
                >
                    // App content ...
                </AppContainer>
            </ValenceProvider>
        </BrowserRouter>
    )
}
```

Above is a minimum example, and there are many other props and options to break down about this component.

### The `nav` prop

The `nav` prop allows you to insert an [`AppNav`](../navigation/nav.md) element, and will render it down the left of the screen (or on the bottom on `mobile` breakpoints). It can be hidden by setting the `showNav` prop to `false`.

***

## Centering page content

As of Valence 3, the App Container no longer handles default page width within the component, instead handing this responsibility off to the developer. To achieve a similar effect to what could be done in Valence 2, use a [Flex Center](flex/flex-center.md) component:

```tsx
import { AppContainer, Header, FlexCenter } from "@valence-ui/core";

function Example() { 
    return ( 
        <AppContainer>
            <Header innerWidth="min(100%, 700px)">
                // Header content...
            </Header>
            <FlexCenter innerWidth="min(100%, 700px)">
                // Page contents...    
            </FlexCenter>
        </AppContainer>
    )
}
```

This change allows greater flexibility in layout and design choices.

***

## Props

_Extends_ [_`GenericLayoutProps`_](./) _&_ [_`PolymorphicLayoutProps`_](../../../valence-utils/generics/polymorphic.md)_._

| Property | Type        | Description                                                                  |
| -------- | ----------- | ---------------------------------------------------------------------------- |
| nav      | `ReactNode` | The primary root navigation element; this should be consistent across pages. |
| showNav  | `boolean`   | Whether to show the `nav` element. Defaults to `true`.                       |

***

## Changelog

* **3.0.0:** Moved the App Container from `@valence-ui/app` to `@valence-ui/core`. This component has also received significant updates:
  * `header` and `sidebar` are no longer accepted as a prop; sidebars are no longer supported and it is the responsibility of the page content to handle any headers.
  * The App Container also no longer handles centering page content; this is now the responsibility of the page to do this.
