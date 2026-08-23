## Overview

Trunk is a WASM web application bundler for Rust. It builds and bundles WASM, JavaScript snippets, and other assets (images, CSS, SCSS) via a source HTML file.

## How it works

- Trunk uses a source HTML file to drive all asset building and bundling.
- It integrates with wasm-bindgen-based frameworks (e.g., Yew, Leptos).
- The build outputs a dist directory containing the HTML, a CSS file, a JavaScript loader, and the WASM binary.

## Usage

1. Create an index.html with trunk data-trunk entries (e.g., link rel=\"scss\" and link rel=\"rust\").
2. Run trunk build to generate dist content.
3. Serve the dist directory from a web server.

## Licensing

Trunk is licensed under the MIT License or the Apache License 2.0, at your choosing.
