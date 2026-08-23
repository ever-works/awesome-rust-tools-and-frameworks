## Overview

Insta is a snapshot testing library for Rust. It allows tests to generate and compare outputs against stored snapshots, which is particularly useful for large or frequently changing data.

## Features

- Snapshot storage and comparison
- Inline snapshots and editor tooling via cargo-insta
- Diffing support through the similar crate

## Example

```rust
fn generate_large_array() -> Vec&lt;u32&gt; { (1..=100).collect() }

#[cfg(test)]
mod tests {
  use super::*;
  #[test]
  fn test_generate_large_array() {
    let array = generate_large_array();
    insta::assert_debug_snapshot!(array);
  }
}
```
