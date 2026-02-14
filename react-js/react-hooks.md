# useState in React

## Basic Syntax

``` js
const [state, setState] = useState(initialValue);
```

-   **state** → Current value\
-   **setState** → Function used to update the value\
-   **initialValue** → Starting value

------------------------------------------------------------------------

## Example

``` jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <>
      <p>{count}</p>
      <button onClick={() => setCount(count + 1)}>
        +
      </button>
    </>
  );
}
```

------------------------------------------------------------------------

## Updating Based on Previous Value (Best Practice)

``` js
setCount(prev => prev + 1);
```

------------------------------------------------------------------------

## Important Note

❌ Never modify state directly:

``` js
count = count + 1; // Wrong
```

✅ Always use the setter:

``` js
setCount(count + 1); // Correct
```

------------------------------------------------------------------------

## Summary

`useState` allows you to:

-   Store dynamic values
-   Update UI automatically
-   Control component behavior
