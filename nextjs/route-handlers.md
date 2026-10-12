# Route handlers (API routes in the App Router)

**Date:** 2026-10-12
**Tags:** nextjs, api

## What I learned

A file named `route.js` inside the `app` folder defines an HTTP endpoint. Export a function named after the HTTP method.

## Example

```js
// app/api/hello/route.js
export async function GET() {
  return Response.json({ message: "Hello" });
}

export async function POST(request) {
  const body = await request.json();
  return Response.json({ received: body }, { status: 201 });
}
```

## Why it matters

Lets the same Next.js project serve both pages and a small backend API, and keeps secret keys on the server.
