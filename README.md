# Config

This repo contains a collection of config files for different types of projects. Each config is a standalone set of files that can be copied to a project and used as is, or modified as needed.

## Available configs

- [Shared](./shared):
  - Shared config for all projects
  - .prettierrc
  - .gitignore
  - .editorconfig
- [NextJS](./next):
  - TypeScript
  - Path aliases (`"@/*"`)
  - ESLint: ignore unnecessary error (`<Image/>` component)
- [Node + TS](./node_express):
  - Support for TypeScript
  - ESM modules
  - Hot reloading using nodemon and ts-node
  - ESLint
  - Path aliases (`"@/*"`) with [tsconfig-paths](https://www.npmjs.com/package/tsconfig-paths)

## How to use

- Copy the desired config to your project
- Modify the config files as needed
- Install the required dependencies
- Start coding!
