# HTTP status codes worth remembering

**Date:** 2026-10-12
**Tags:** http, debugging

## What I learned

- **200** OK, **201** Created, **204** No Content
- **301** moved permanently, **302** temporary redirect
- **400** bad request, **401** not authenticated, **403** authenticated but not allowed, **404** not found
- **429** too many requests
- **500** server error, **502** bad gateway, **503** service unavailable

## Why it matters

The code tells you where to look first: 4xx usually means the request or permissions, 5xx means the server side.
