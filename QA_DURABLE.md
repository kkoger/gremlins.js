# QA_DURABLE

## Dependency Installation

The project uses npm for dependency management. The `package.json` defines the following dev dependencies:
- webpack (^1.8.11)
- webpack-dev-server (^1.8.2)

To install dependencies, run:
```bash
npm install
```

This will install the dependencies specified in package.json.

## Verification

The `npm test` script in package.json maps to `make test`. However, inspecting the Makefile reveals that there is no `test` target defined. The Makefile only contains three targets:
- `watch`: Runs webpack-dev-server with colors and progress indicators
- `setup`: Installs npm dependencies
- `build`: Builds the project with webpack in production mode

The `test` target referenced by `npm test` does not exist in the Makefile, which means running `npm test` will fail unless a `test` target is added to the Makefile.

Reconnect verification completed.
