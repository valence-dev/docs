---
description: 'Last updated: v2.0.0 (16/01/2023)'
---

# 🍏 The AppContainer

The `AppContainer` is a powerful all-in-one component that, as the name suggests, creates a container in which the content of the app resides. It is designed to be responsive across all device ranges, but takes a great deal of creative liberties in terms of layout and styling.

## Usage

```tsx
import { AppContainer, Nav } from "@valence-ui/app";
import { Button, Header } from "@valence-ui/core";
import { BrowserRouter } from "react-router-dom";
import { IconCategory } from "@tabler/icons-react";

export default function App() { 
    return ( 
        <BrowserRouter>
            <ValenceProvider>
                <AppContainer
                    nav={
                        <Nav
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
                    header={
                        <Header>
                            // Page header...
                        </Header>
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

The `nav` prop allows you to insert a [`Nav`](components/navigation/nav.md) element, and will render it down the left of the screen (or on the bottom on `mobile` breakpoints).

The `Nav` prop is _required_, but can be hidden using the `showNav` prop.

The `header` prop allows you to insert an element to act as the page's header, which in most cases should be the `Header` component. This `Header` should contain a `Title` or `h1` element, like so:

```tsx
import { AppContainer } from "@valence-ui/app";
import { Header, Title } from "@valence-ui/core";

// other props...
function Example() { 
    return ( 
        <AppContainer
            header={
                <Header>
                    <Title>
                        Page title
                    </Title>
                </Header>
            }
        >
            // Children...
        </AppContainer>
    )
}
```

Like the `nav`, the `header` is required.

### The `sidebar` prop

The `sidebar` prop, unlike its siblings `nav` and `header`, is not required. It provides a space to insert a [`Sidebar` ](components/navigation/sidebar.md)component, and should be used for page-level navigation and actions.

***

## Understanding application hierarchy

The visual design and layout of the `AppContainer` creates a hierarchy within the application that should be followed to help your users easily navigate your page and app as a whole.

1. **The `Nav` component** is the highest level on this hierarchy, and should be handling application-level actions and navigation, such as:\
   \- Page navigation\
   \- Signing out of the app\
   \- Changing global settings (color scheme, etc.)
2. **The `Sidebar` component** is a page-level element designed to be used for high-level actions relating to _that page only_. This includes things such as:\
   \- Jumping between anchors on the page\
   \- Saving, loading or searching for content visible on the page
3. **The `Header` component** should provide a title or high-level actions for the page. Notably, minimal interactive content should be kept here, as this will be in the top 15-20% of a user's device on `mobile` breakpoints, thus making it difficult to reach.

***

## Modifying content width

The main content of the page defaults to a maximum width of `700` pixels, but this can be modified with the `contentWidth` prop:

```tsx
import { AppContainer } from "@valence-ui/app";

// other props...
function Example() { 
    return ( 
        <AppContainer
            // Other required props...
            contentWidth={700}
        >
            // Children...
        </AppContainer>
    )
}
```

All elements encapsulated within the page's main content container will be centered in the remaining whitespace of the page (that is, anything not taken up by the `Nav`, `Sidebar` and `SideSheet` components).&#x20;

You may also pass additional props onto this container with the `pageProps` prop.
