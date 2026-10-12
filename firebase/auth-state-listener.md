# Firebase Auth: onAuthStateChanged

**Date:** 2026-10-12
**Tags:** firebase, auth, javascript

## What I learned

`auth.currentUser` is `null` right after page load because Firebase restores the session asynchronously. Use `onAuthStateChanged` to react when the user is known.

## Example

```js
import { onAuthStateChanged } from "firebase/auth";

const unsubscribe = onAuthStateChanged(auth, (user) => {
  if (user) {
    console.log("Signed in:", user.uid);
  } else {
    console.log("Signed out");
  }
});

// call unsubscribe() when the component unmounts
```

## Why it matters

Avoids flashing the login page for users who are already signed in.
