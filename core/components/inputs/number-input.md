# Number input
The `NumberInput` is a controlled wrapper component around the `input=number` html component.

## Props
Extends [`GenericInputProps` and `GenericInputEventHandlerProps`](./input-container.md).
| Property     | Type                                   | Description                                                       |
|--------------|----------------------------------------|-------------------------------------------------------------------|
| value        | `number`                               | The value of this input (required).                               |
| setValue     | `Dispatch<SetStateAction<number>>`     | Sets the value of this input (required).                          |
| min          | `number`                               | The minimum value of this input.                                  |
| max          | `number`                               | The maximum value of this input.                                  |
| step         | `number`                               | The step value of this input. Defaults to `1`.                    |
| showControls | `boolean`                              | Whether the stepper controls should be shown. Defaults to `true`. |
| controlIcons | `{ up?: ReactNode, down?: ReactNode }` | Sets custom icons for the stepper control buttons.                |

## About control
By default, all Valence inputs are controlled. The input components do not accept event handlers for the `setValue` props, instead accept the direct `setState` return values, like so: 

```ts
import { useState } from "react";
import { NumberInput } from "valence-ui";

function Demo() { 
  const [value, setValue] = useState(0);

  return ( 
    <NumberInput 
      value={value}
      setValue={setValue}
    />
  )
}
```