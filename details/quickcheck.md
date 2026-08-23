## Overview

QuickCheck is a property-based testing framework for Rust. It generates random inputs to test that a property holds for all inputs and shrinks a counterexample when a failure is found.

## Example

```rust
// Basic example showing a property-based test for reversing a vector
#[cfg(test)]
#[macro_use]
extern crate quickcheck;

fn reverse<T: Clone>(xs: &[T]) -> Vec<T> { xs.iter().rev().cloned().collect() }

#[cfg(test)]
mod tests {
  quickcheck! {
    fn prop(xs: Vec<u32>) -> bool { xs == reverse(&reverse(&xs)) }
  }
}
```
