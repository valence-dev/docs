# `useDefaultIconProps`
Designed out of a need to standardise Tabler icon props, this hook exists to do exactly that. 

## Usage
```ts
import { useDefaultIconProps } from "valence-ui";

function Demo() { 
  const defaultIconProps = useDefaultIconProps();

  return ( 
    <IconChevronUp
      {...defaultIconProps.get()}
    />
  )
}
```

The `.get()` method accepts two optional parameters; `color?: string` and `size?: number`. The color string can be used to reference any Valence color. If they are not supplied, the function will return an icon with a size of `20` and an undefined color. 