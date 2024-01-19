---
description: 'Last updated: 2.0.0 (19/01/2024)'
---

# Alert

## Usage

```tsx
import { Alert } from "@valence-ui/core";
import { IconAlertCircle } from "@tabler/icons-react";

function MyComponent() { 
    const [show, setShow] = React.useState(true);

    return ( 
        <Alert
            alert={{
                title: "Alert title",
                message: "Alert message",
                icon: <IconAlertCircle />,
            }}
            show={show}
        />
    )
}
```

### Controlled alert content

```tsx
import { Alert, AlertContent } from "@valence-ui/core";
import { IconAlertCircle } from "@tabler/icons-react";

function MyComponent() { 
    const [alert, setAlert] = React.useState<AlertContent | null>({
        title: "Alert title",
        message: "Alert message",
        icon: <IconAlertCircle />,
    });

    return ( 
        <Alert
            alert={alert}
            show={alert !== null}
        />
    )
}
```

### Actions on click

```tsx
import { Alert } from "@valence-ui/core";
import { IconAlertCircle } from "@tabler/icons-react";

function MyComponent() { 
    
    function handleClick() { 
        console.log("Alert was clicked!");
    }

    return ( 
        <Alert
            alert={{
                title: "Alert title",
                message: "Alert message",
                icon: <IconAlertCircle />,
            }}
            show={true}
            onClick={handleClick}
        />
    )
}
```

{% hint style="info" %}
Other button attributes and behaviors can be passed to the Alert as well.
{% endhint %}

### Alert levels

The `variant` prop can be used to display the alert with different appearances. These variants can be used to create awareness and urgency in the alert, which may be useful when displaying errors, etc.

1. `"filled"` makes the alert very visible, which is useful for displaying major errors.\
   E.g. input validation error, save failure, etc.
2. `"light"` draws attention to the alert, but with a softness that is more suitable for positive updates or minor errors.\
   E.g. successful save, non-breaking error, etc.
3. `"subtle"` is the least attention-grabbing of the three, and is best used for very minor alerts.\
   E.g. additional information about an action, ideal input content, etc.

***

## Props

_Extends `GenericClickableProps`, `GenericClickableEventProps`, `PolymorphicButtonProps` and `GenericLayoutProps`._

<table data-full-width="true"><thead><tr><th width="164">Property</th><th width="237">Type</th><th>Description</th></tr></thead><tbody><tr><td>alert (required)</td><td><code>AlertContent</code></td><td>The content of this alert.</td></tr><tr><td>show</td><td><code>boolean</code></td><td>Whether to mount and show this alert.</td></tr><tr><td>variant</td><td><code>FillVariant</code></td><td>The styling variant of this alert. Defaults to <code>filled</code>.</td></tr><tr><td>size</td><td><code>ComponentSize</code></td><td>The size of this alert. Defaults to the theme default size.</td></tr><tr><td>radius</td><td><code>ComponentSize</code></td><td>The border size of this alert. Defaults to the theme default radius size.</td></tr><tr><td>shadow</td><td><code>boolean</code></td><td>Specifies if a shadow will be shown.</td></tr><tr><td>motion</td><td><code>MotionBehaviourProps</code></td><td>Defines motion behavior for this button. This will automatically be overridden if the user has reduced motion enabled on their device.</td></tr></tbody></table>

## AlertContent

<table data-full-width="true"><thead><tr><th width="158">Property</th><th width="133">Type</th><th>Description</th></tr></thead><tbody><tr><td>title (required)</td><td><code>string</code></td><td>The title of this alert.</td></tr><tr><td>message</td><td><code>string</code></td><td>The message of this alert.</td></tr><tr><td>icon</td><td><code>ReactNode</code></td><td>The icon of this alert.</td></tr></tbody></table>
