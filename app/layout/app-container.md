# `AppContainer`
The `AppContainer` component is a large component that handles the layout of an entire app page, including the [`Nav`](../layout/nav.md) and [`Sidebar`](../layout/sidebar.md) components and page content.

## Interaction hierarchy
The visual design of the `AppContainer` creates an interaction hierarchy that should be followed for ease-of-use. 
1. The `Nav` component is designed to handle root page navigation and app-level functions. That is, the `Nav` should be nearly identical across every page in an app and should contain functions that are identical across every page. Examples of such functions include signing out of the app or managing basic account settings.
2. The `Sidebar` component is an optional one that is used for in-page navigation and high-level functions. This component should **not** be used to navigate to other pages, nor should it change dramatically based upon the state of the page's content. Examples of good uses for this component include jumping to heading anchors or changing information displayed on a page.
3. The `Header` component will change location based upon a few criteria. If the `Sidebar` is provided, it will appear above the regular sidebar content on desktop devices, but otherwise it will appear at the top of the regular page content. The `Header` should contain a `Title` or `h1` for this page's content.
4. All other page content should be passed into the `children` prop and will be displayed on the root page element.

On desktop devices, the navigation will be sorted from left to right, with the `Nav` component on the very left. On mobile devices, the layout will be flipped such that the `Nav` becomes horizontal along the bottom, and the default `Sidebar` component is transformed and displayed horizontally above the `Nav`. 


## Props
| Property          | Type                         | Description                                                                               |
|-------------------|------------------------------|-------------------------------------------------------------------------------------------|
| nav               | `ReactNode`                  | The primary root page navigation element (required).                                      |
| header            | `ReactNode`                  | The header containing the `<h1>` element for this page (required).                        |
| sidebar           | `ReactNode`                  | An optional sidebar element used for navigation or page-level actions.                    |
| radius            | `ComponentSize`              | The border radius of the page container. Defaults to `5px` larger than the theme default. |
| navContainerProps | `GenericReactiveLayoutProps` | Properties to apply to the nav container element.                                         |
| pageProps         | `GenericReactiveLayoutProps` | Properties to apply to the page container element.                                        |
| contentWidth      | `number`                     | The maximum width of this page's content. Defaults to `700`.                              |
| sidebarWidth      | `number`                     | The width of the sidebar element. Defaults to `270`.                                      |
| navWidth          | `number`                     | The width of the nav element. Defaults to `65`.                                           |