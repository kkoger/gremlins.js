# Contributing to gremlins.js

Thank you for your interest in contributing to gremlins.js! This document explains how to set up your development environment and build the project.

## Installation

First, install the project dependencies using npm:

```bash
npm install
```

Or use the provided Makefile target:

```bash
make setup
```

## Building

To build the minified production version of the library, run:

```bash
make build
```

This compiles the source files using webpack in production mode and generates `gremlins.min.js`.

## Development

To start the webpack development server with live reloading, run:

```bash
make watch
```

This will start a development server with file watching and hot module replacement.

## Testing

**Note:** The project does not currently have a dedicated test target in the Makefile. To verify your changes, test the library against the bundled examples:

- **Basic example:** `examples/basic/index.html`
- **TodoMVC example:** `examples/TodoMVC/index.html`
- **Touch example:** `examples/touch/index.html`

Open these HTML files in a browser to manually verify that gremlins behave as expected.

## Contributing Guidelines

When contributing new features or fixes:

1. Follow the functional programming style used in the codebase
2. Test your changes against the bundled examples
3. Rebuild the minified version using `make build` before submitting your pull request
4. New gremlins, mogwais, and strategies should be thoroughly tested with the examples

## Project Structure

- `src/` - Source code for gremlins, mogwais, strategies, and utilities
- `src/species/` - Gremlin species (clicker, formFiller, scroller, toucher, typer)
- `src/mogwais/` - Mogwais (alert, fps, gizmo)
- `src/strategies/` - Execution strategies (allTogether, bySpecies, distribution)
- `examples/` - Example applications demonstrating gremlins.js usage
- `gremlins.min.js` - Minified production build
