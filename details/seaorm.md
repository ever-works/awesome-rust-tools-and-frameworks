## Overview
SeaORM is a fully async-friendly Rust ORM built on SQLx that abstracts raw SQL away to provide a clean interface using structs as models, with derive macros and traits. It includes a CLI for generating migrations, entities, and models, and features an ActiveModel system to extend behavior before or after saving a record. SeaORM auto-generates structs from your schema and works well with Axum. A new framework called Loco uses SeaORM to approximate the Rails experience in Rust by leveraging SeaORM traits.

## Features
- Async-friendly ORM built on SQLx
- Derive macros and traits for models
- CLI for migrations, entities, and models
- ActiveModel extension points before/after saving
- Auto-generates structs from schema
- Interoperates with Axum and other frameworks
- Supports raw SQL escape hatches
- Runtime checks vs compile-time checks (SeaORM does not provide compile-time type checks like Diesel)

## Performance & Tradeoffs
- Faster compilation times than Diesel for basic use
- Generally slower than Diesel at runtime; larger binaries

## Using SeaORM with Shuttle
By default, Shuttle provides a SQLx connection from the shared_db crate which can be turned into a SeaORM connection. In production, Shuttle can provision a Postgres instance automatically.

## Limitations & Considerations
- Migration files can be very long
- The Iden derive macro documentation is not clearly explained
