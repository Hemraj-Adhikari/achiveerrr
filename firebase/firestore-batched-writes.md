# Firestore batched writes

**Date:** 2026-10-12
**Tags:** firebase, firestore

## What I learned

A batched write groups several writes into one atomic operation: either all succeed or none do. A single batch can contain up to 500 operations.

## Example

```js
import { writeBatch, doc } from "firebase/firestore";

const batch = writeBatch(db);
batch.update(doc(db, "tasks", "a1"), { status: "done" });
batch.update(doc(db, "tasks", "a2"), { status: "done" });
batch.delete(doc(db, "tasks", "old1"));
await batch.commit();
```

## Why it matters

Keeps related data consistent, for example when updating a lead and its activity log together.
