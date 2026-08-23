## Overview
Diesel-async adds asynchronous support to Diesel, preserving the same compile-time safe DSL while enabling async/await style queries and integration with async runtimes. It includes built-in pooling via bb8 and deadpool.

## Setup
```toml
[dependencies]
diesel = { version = "2", features = ["postgres"] }
diesel-async = { version = "0.8", features = ["postgres", "bb8"] }
tokio = { version = "1", features = ["full"] }
```

## Using
```rust
use diesel_async::pooled_connection::bb8::Pool;
use diesel_async::AsyncPgConnection;
// create pool and obtain AsyncPgConnection, then use await on queries
```

## When to Use
- You are committed to Diesel's DSL but need non-blocking I/O in async web apps.

## Trade-offs
- Async support is via extra crate (diesel-async).
- Still requires synchronization with schema.rs; no full runtime cost savings from dropping the ORM layer.
