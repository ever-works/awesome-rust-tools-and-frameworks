## Overview

log is a lightweight logging facade that provides a single API that abstracts over the actual logging backend. It lets you emit log messages and relies on a separate logger crate for the actual output. Maintained by the official Rust team, it is widely used as a foundational crate for Rust logging.

## Usage

In typical usage you set the log level and emit messages; the concrete logger behind the facade handles the output.