# Share configs

These configs are shared across all projects.

## [.prettierrc](https://prettier.io/)

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

### How to use prettier config

- Copy the `.prettierrc` file to the root of the project
- Install the required dependencies
- Start coding!

## [.gitignore](https://git-scm.com/docs/gitignore)

Standard configuration for files and directories to be ignored by Git.

Including but not limited to:

- `node_modules`
- `.DS_Store`
- `.env*.local`
- All build directories (`dist`, `build`, `out`, `.next`, etc.)

## [.editorconfig](https://editorconfig.org/)

Standard configuration for code editors. Including recommended extensions for VSCode.

## [pre-commit](https://pre-commit.com/)

Configuration for pre-commit hooks that runs before each commit. Can be used to run tests, linting, formatting, etc.

The `pre-commit.sh` hook can be used with any githooks implementation. This example uses [husky](https://typicode.github.io/husky/).

### Current config

- Run format with Prettier on staged files `yarn format`
- Add them to the commit using `git add .`
- (Optional) Run lint with ESLint on staged files `yarn lint`

### How to use husky with pre-commit

The `husky` package must be installed as `devDependencies` in the project.

```bash
npm install --save-dev husky
```

OR

```bash
yarn add --dev husky
```

Add the following to the `package.json`:

```json
{
  "scripts": {
    "prepare": "husky",
    "format": "prettier --write . --config ./.prettierrc"
  }
}
```
