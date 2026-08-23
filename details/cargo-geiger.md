## Overview

Cargo-geiger is a cargo subcommand that analyzes Rust dependencies to detect usage of unsafe code, helping identify potential security risks. It is invoked as cargo geiger and integrates into the Rust toolchain.

## Features
- Scans crates for unsafe blocks across dependencies
- Reports on potential safety issues and areas to review
- Integrates with standard cargo workflow