---
description: 'Last updated: 2.0.0 (19/01/2024)'
---

# Accordion

## Usage

```tsx
import { Accordion, useControlledList } from "@valence-ui/core";

function MyComponent() { 
    const openedItems = useControlledList(["item1"]);

    return ( 
        <Accordion
            itemList={openedItems}
        >
            <Accordion.Item
                key="item1"
                value="item1"
                control={
                    <Accordion.Control
                        title="Item 1"
                    />
                }
            >
                <Accordion.Panel>
                    // Accordion child contents...
                </Accordion.Panel>
            </Accordion.Item>
            
            // Additional accordion items...
        </Accordion>
    )
}
```

All items passed into the `useControlledList()` hook will determine which items are initially "opened". You can supply as few or as many items to this list as you'd like.&#x20;

## Props

### AccordionProps

_Extends `FlexProps`._

<table data-full-width="true"><thead><tr><th width="185">Property</th><th width="254">Type</th><th>Description</th></tr></thead><tbody><tr><td>itemList (required)</td><td><code>ControlledList&#x3C;string></code></td><td>The list of items associated with this accordion.</td></tr><tr><td>children (required)</td><td><code>ReactNode[]</code></td><td></td></tr></tbody></table>

### AccordionItemProps

_Extends `FlexProps`._&#x20;

<table data-full-width="true"><thead><tr><th width="176">Property</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td>value (required)</td><td><code>string</code></td><td>The value of this accordion item.</td></tr><tr><td>control (required)</td><td><code>ReactNode</code></td><td>The control to display for this item.</td></tr><tr><td>flexProps</td><td><code>FlexProps</code></td><td>Props to apply to the Flex element surrounding the children.</td></tr></tbody></table>

### AccordionControlProps

_Extends `FlexProps`._

<table data-full-width="true"><thead><tr><th width="153">Property</th><th width="138">Type</th><th>Description</th></tr></thead><tbody><tr><td>title (required)</td><td><code>string</code></td><td>The title to display in the control.</td></tr><tr><td>chevronIcon</td><td><code>ReactNode</code></td><td>The icon to display in the control.</td></tr><tr><td>titleProps</td><td><code>TitleProps</code></td><td>Optional props to pass to the title.</td></tr><tr><td>opened</td><td><code>boolean</code></td><td>Whether the control is opened</td></tr></tbody></table>

### AccordionPanelProps

_Extends `FlexProps`._

> No unique props.
