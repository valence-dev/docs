# `useDetectKeyDown`
This hook allows the execution of a callback function on the detection of one or more keys.

## Usage
```ts
import { useDetectKeyDown } from "valence-ui";

function Demo() { 

  function callback() {
    console.log("Hi there!");
  }

  useDetectKeyDown(
    callback,     // The function to call
    "Escape",     // Can be a string or list of strings
    true,         // Used for controllable checking
    [callback]    // Any relevant dependencies
  );
}
```