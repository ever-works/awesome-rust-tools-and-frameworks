## Overview

Rustfmt is the community standard for code style. It reformats your source files to match a strict set of rules and is invoked via cargo fmt. The default configuration is the convention, but a rustfmt.toml config file can be used (and if configured, should be committed to CI).

## Features
- Automatic formatting of Rust source files to a consistent style
- Deterministic output across environments
- Configurable via rustfmt.toml (optional) and enforced by CI

## Usage
- Run: cargo fmt