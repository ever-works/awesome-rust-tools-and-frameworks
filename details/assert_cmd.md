## Overview

Assert_cmd provides utilities to run a compiled binary and make assertions about its behavior, enabling reliable integration testing of command-line interfaces.

## Example

```rust
use assert_cmd::Command;

let mut cmd = Command::cargo_bin("my-cli-app").unwrap();
cmd.assert().success();
```
