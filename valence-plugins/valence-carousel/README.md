---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# 🎠 Valence Carousel

{% hint style="warning" %}
This package is a Plugin package, meaning that it is designed to function alongside your chosen Discipline package, and should not be used alone. [Don't know what this means?](../../overview/getting-started.md)
{% endhint %}

The Valence Carousel is a custom horizontal carousel component designed for maximum usability in desktop and mobile environments. It allows a user to interact with it via the browser's native horizontal scroll, by clicking and dragging, and with the controls on either side. This component is based closely on the image carousel in the Instagram Threads app.

## Installation & usage

```bash
npm install @valence-ui/carousel
```

```tsx
import { Carousel, CarouselChildProps } from "@valence-ui/carousel";

function Demo() { 
  return (
    <Carousel>
      <CarouselChild 
        key={i}
      />
    </Carousel>
  )
}

function CarouselChild(props: CarouselChildProps) { 
  return ( 
    <div
      style={{
        backgroundColor: props.isActive ? "red" : undefined,
        outline: props.isNearest ? "1px solid red" : undefined,
      }}
    >
      Carousel Child
    </div>
  )
}
```

This example is an uncontrolled carousel. The Carousel package does not include a default child component, instead relying on a custom component that uses the `CarouselChildProps`. `CarouselChildProps` gives the `isActive` and `isNearest` props to the child, which can be used to influence style or behaviour.

The Carousel can also be used in a controlled manner, allowing higher-level components to know and/or control the active child:

```tsx
import { Carousel, CarouselChildProps } from "@valence-ui/carousel";
import { useState } from "react";

function Demo() { 

  const [activeChild, setActiveChild] = useState(0);

  return (
    <Carousel
      activeChild={activeChild}
      setActiveChild={setActiveChild}
    >
      <CarouselChild 
        key={i}
      />
    </Carousel>
  )
}

// etc.
```
