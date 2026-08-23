## Overview

Criterion.rs is a powerful and statistically-driven benchmarking library for Rust that detects even the smallest performance changes in your code. It supports HTML reports and can generate plots via gnuplot or plotters, offering a robust framework for performance analysis.

## Getting Started

1. Create a new Rust project: `cargo new your-benchmark-project`
2. Add Criterion as a development dependency with HTML reports:

```
cargo add -D criterion -F html_reports
```

3. Update Cargo.toml to enable html_reports:

```
[dev-dependencies]
criterion = { version = "0.5.1", features = ["html_reports"] }
```

4. Create a benches/ directory and a benchmark file (e.g., benches/sort_benchmarks.rs) containing your benchmark using Criterion's API.

```
use criterion::{criterion_group, criterion_main, Criterion};

fn criterion_benchmark(c: &mut Criterion) {
    // your benchmarks here
}

criterion_group!(benches, criterion_benchmark);
criterion_main!(benches);
```

5. Run benchmarks with `cargo bench`. Criterion collects statistics and generates HTML reports.

## HTML Reports

When you run benchmarks with html_reports, Criterion outputs HTML reports under `target/criterion/report/index.html`, with plots available if gnuplot is installed. If gnuplot isn't available, Criterion uses the plotters backend for rendering graphs.

## Features

- Statistical analysis (mean, median, standard deviation, confidence intervals)
- Compare two functions or two sets of inputs
- Custom measurements and timing loops
- Outputs include HTML reports and charts

## Optional: Installing Gnuplot (Linux)

To enable detailed plots, install gnuplot:

```
sudo apt update
sudo apt install gnuplot
```

## Conclusion

Criterion.rs is a mature, open-source benchmarking tool for Rust, providing robust statistical analysis and convenient HTML reports to understand performance characteristics of code.