# mdserve

A lightweight Rust Markdown preview server with live reload, themes, Mermaid diagrams, and KaTeX math rendering.

`mdserve` serves Markdown files locally and renders them in your browser. Edit a file and see the updated result without manually refreshing the page.

This is the independent **ocodo hard fork** of jfernandez/mdserve, maintained with a focus on a useful, clean reading and writing experience.

## Features

- **Live reload** — updates the preview when Markdown files change.
- **Markdown rendering** — tables, task lists, fenced code blocks, and other supported Markdown syntax.
- **Math rendering** — KaTeX for inline and display mathematics.
- **Mermaid diagrams** — render diagrams in Markdown documents.
- **Directory mode** — browse Markdown files using a sidebar.
- **Themes** — light, dark, and Catppuccin themes.
- **Local-first** — serves your documents from your own machine.

## Installation

Install the latest version directly from GitHub with Cargo:

```
cargo install --git https://github.com/ocodo/mdserve --force
```

To build from source:

```
git clone https://github.com/ocodo/mdserve.git
cd mdserve
cargo install --path .
```

The executable is installed to Cargo's binary directory, usually `~/.cargo/bin`.


## Usage

Serve a single Markdown file:

```
mdserve README.md
```

Serve a directory of Markdown files:

```
mdserve docs/
```

Choose a port:

```
mdserve README.md --port 8080
```

Open the preview in your browser automatically:

```
mdserve README.md --open
```

Run `mdserve --help` for available options.

## Mathematics

Inline mathematics:

```
Euler's identity is $ e^{i\pi} + 1 = 0 $.
```

e.g. 

Euler's identity is $ e^{i\pi} + 1 = 0 $.

Display mathematics:

```
$$
\int_0^1 x^2\,dx = \frac{1}{3}
$$
```

$$
\int_0^1 x^2\,dx = \frac{1}{3}
$$


Math is rendered in the browser using KaTeX. The current template loads KaTeX from a CDN, so an internet connection is required to download its assets.

## Building and testing

Requires Rust and Cargo.

```
cargo build --release
cargo test
```

## Lineage

This project began as a fork of jfernandez/mdserve and is now maintained independently under the `ocodo` namespace. The upstream project and this fork may diverge.

See CHANGELOG.md for the fork's development history.

## License

See LICENSE for the applicable license.
