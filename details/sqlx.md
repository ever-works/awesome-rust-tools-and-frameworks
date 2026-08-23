## Overview
SQLx is an asynchronous Rust library that lets you write raw SQL with compile-time checking via query! and query_as! macros. It supports Postgres, MySQL, and SQLite, with connection pooling. It integrates with web frameworks like Axum and Actix.

## Features
- Async runtime compatible
- Compile-time SQL verification with query!/query_as!
- Multi-database support (Postgres, MySQL, SQLite)
- Migrations via sqlx-cli
- Transparent, direct SQL execution

## Usage with Shuttle
Shuttle supports SQLx via the shuttle-shared-db crate; local Postgres is spun up in Docker during development, and Shuttle provisions managed databases in production. The sqlx::migrate!() macro runs migrations from the migrations/ directory at startup.