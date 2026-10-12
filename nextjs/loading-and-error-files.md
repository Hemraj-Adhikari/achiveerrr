# loading.js and error.js in the App Router

**Date:** 2026-10-12
**Tags:** nextjs, ux

## What I learned

Special files inside a route folder add UI states automatically:

- `loading.js` is shown while the page's data is loading
- `error.js` is shown when something in that route throws, and it must be a client component
- `not-found.js` is shown when `notFound()` is called

## Example

```jsx
// app/tasks/error.js
"use client";

export default function Error({ error, reset }) {
  return (
    <div>
      <p>Something went wrong.</p>
      <button onClick={() => reset()}>Try again</button>
    </div>
  );
}
```

## Why it matters

Gives users clear feedback without writing loading and error handling in every page.
