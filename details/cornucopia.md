## Overview
Cornucopia takes a unique approach: you write SQL in .sql files, and it generates type-safe Rust code from those queries. It's similar to sqlc in the Go world. You write a query file:

--! get_published_posts
SELECT id, title, body, published
FROM posts
WHERE published = :published
ORDER BY id DESC
LIMIT :limit;

Then Cornucopia generates Rust functions with the correct types. No macros, no runtime overhead - just generated code.

## Good for
Teams that want SQL-first development with zero runtime cost. The generated code is easy to audit.

## Tradeoffs
PostgreSQL only. Smaller community than the big three.
