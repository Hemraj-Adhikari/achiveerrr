# Firestore composite indexes

**Date:** 2026-10-12
**Tags:** firebase, firestore, queries

## What I learned

Firestore creates indexes for single fields automatically. A query that filters or sorts on several fields (for example `where("status", "==", "open")` together with `orderBy("createdAt")`) needs a composite index that you create yourself.

## Example

When such a query runs without its index, the error message in the console contains a link. Opening that link pre-fills the index in the Firebase console, and you only need to confirm and wait for it to build.

## Why it matters

Explains the common "The query requires an index" error and how to fix it quickly.
