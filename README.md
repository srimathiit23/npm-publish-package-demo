# npm-packaging

A local npm package for testing package publishing to Verdaccio registry.

## Overview

This package demonstrates:
- Local package development with ES modules
- Using the `consice-logger` local dependency
- Publishing to a local Verdaccio registry
- Testing package installation from local registry

## Installation

```bash
npm install npm-packaging --registry http://localhost:4873
```

## Usage

```javascript
import { logger } from 'npm-packaging';
```

Or run the test directly:

```bash
npm test
# or
npm start
```

## Features

- ES module support (`"type": "module"`)
- Local dependency management (`consice-logger`)
- Configured for Verdaccio registry publishing
- Includes test script

## Publishing to Local Registry

```bash
# Make sure Verdaccio is running
npx verdaccio

# In another terminal, publish the package
npm publish --registry http://localhost:4873
```

## Testing Local Package

```bash
# After publishing, test installation
npm install npm-packaging@1.0.0 --registry http://localhost:4873
```

## Package Details

- **Version**: 1.0.0
- **Type**: ES Module
- **Main Entry**: test.js
- **Registry**: http://localhost:4873 (local Verdaccio)

## License

ISC
