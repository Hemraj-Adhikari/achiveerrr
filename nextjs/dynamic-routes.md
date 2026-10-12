# Next.js dynamic routes (App Router)

**Date:** 2026-10-12
**Tags:** nextjs, routing

## What I learned

A folder name in square brackets creates a dynamic segment. `app/tasks/[id]/page.js` matches `/tasks/1`, `/tasks/abc`, and so on.

## Example

```jsx
// app/tasks/[id]/page.js
export default async function TaskPage({ params }) {
  const { id } = await params;
  return <h1>Task {id}</h1>;
}
```

In recent versions of Next.js, `params` is a Promise, so it is awaited.

## Why it matters

One page file handles every item without creating a route per record.
