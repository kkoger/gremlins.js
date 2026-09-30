# Contributing to gremlins.js

## Installation

To get started with development, install the project dependencies:

```bash
npm install
```

This will install the required dev dependencies including webpack and webpack-dev-server.

## Running Tests

The `npm test` command is configured to run `make test` via the npm scripts in `package.json`. However, note that the Makefile does not currently have a `test` target defined. The available Makefile targets are:

- `make setup` - Install dependencies
- `make build` - Build the production bundle
- `make watch` - Start the webpack dev server

If you need to run tests, you may need to add a test target to the Makefile or run your test command directly.

## Pull Requests

Keep pull requests focused on one change.
