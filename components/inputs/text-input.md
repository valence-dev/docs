# Text input
The `TextInput` component is a powerful controlled wrapper component over the `input=text` html element. 

## Props
Extends [`GenericInputProps` and `GenericInputEventHandlerProps`](./input-container.md).
| Property     | Type                               | Description                                                            |
|--------------|------------------------------------|------------------------------------------------------------------------|
| value        | `number`                           | The value of this input (required).                                    |
| setValue     | `Dispatch<SetStateAction<number>>` | Sets the value of this input (required).                               |
| type         | `TextInputType`                    | The type of input to render. Defaults to `text`.                       |
| autoComplete | `AutoCompleteBehaviour`            | The autocomplete behaviour to use. Defaults to `off`.                  |
| pattern      | `string`                           | A regex pattern to use for input validation.                           |
| minLength    | `number`                           | The minimum character length of this input.                            |
| maxLength    | `number`                           | The maximum character length of this input.                            |
| multiple     | `boolean`                          | If `type=email`, this specifies if this input accepts multiple values. |

### `TextInputType`
Defines the type of input this text input can be.
```ts
"text" | "password" | "email" | "number" | "tel" | "url" | "search"
```

### `AutoCompleteBehaviour`
Defines the type of autocomplete behaviour that will be used.
```ts
"off" | "on" | "name" | "honorific-prefix" | "given-name" | "addtional-name" | "family-name" | "honorific-suffix" | "nickname" | "email" | "email" | "username" | "new-password" | "current-password" | "one-time-code" | "organization-title" | "organization" | "street-address" | "shipping" | "billing" | "address-line1" | "address-line2" | "address-line3" | "address-level4" | "address-level3" | "address-level2" | "address-level1" | "country" | "country-name" | "postal-code" | "cc-name" | "cc-given-name" | "cc-additional-name" | "cc-family-name" | "cc-number" | "cc-exp" | "cc-exp-month" | "cc-exp-year" | "cc-csc" | "cc-type" | "transaction-currency" | "transaction-amount" | "language" | "bday" | "bday-day" | "bday-month" | "bday-year" | "sex" | "tel" | "tel-country-code" | "tel-national" | "tel-area-code" | "tel-local" | "tel-extension" | "impp" | "url" | "photo" | "webauthn"
```


## About control
By default, all Valence inputs are controlled. The input components do not accept event handlers for the `setValue` props, instead accept the direct `setState` return values, like so: 

```ts
import { useState } from "react";
import { TextInput } from "valence-ui";

function Demo() { 
  const [value, setValue] = useState("");

  return ( 
    <TextInput 
      value={value}
      setValue={setValue}
    />
  )
}
```