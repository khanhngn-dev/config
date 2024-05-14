# Share configs

These configs are shared across all projects. They include:

- `.prettierrc`
- `.gitignore`
- `.editorconfig`

## [Prettier](https://prettier.io/)

Standard configuration for code formatting.

Include the use of `@trivago/prettier-plugin-sort-import` to sort imports.

> **Note**: The `@trivago/prettier-plugin-sort-import` plugin must be installed as `devDependencies` in the project.

```bash
npm install --save-dev @trivago/prettier-plugin-sort-imports
```

OR

```bash
yarn add --dev @trivago/prettier-plugin-sort-imports
```

Current order of imports:

```javascript
// 3rd party
import React from 'react';
import { render } from 'react-dom';

// Path aliases
import App from '@/App';

// Relatives
import './index.css';
```