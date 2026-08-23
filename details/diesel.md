## Overview
Diesel is a Rust ORM-like data mapper and query builder with compile-time checks via table! macros. It supports migrations and provides a way to query through structs, but explicit model-layer concepts are less emphasized. It is used at scale, including crates.io via diesel-async.

## Features
- Compile-time safety with table! macros
- Migrations support
- Query builder style with type safety
- Sync-first with async adapters via diesel-async or diesel-deadpool
- Extensive docs and community resources

## Trade-offs
- Steeper learning curve; heavy generic usage
- Focus on type safety and database-specific features rather than portability

## Using Diesel with Shuttle
A community plugin allows using Diesel with Shuttle via diesel-async.