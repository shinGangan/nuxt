---
title: "nuxi module"
description: "Search and add modules to your Nuxt application with the command line."
links:
  - label: Source
    icon: i-simple-icons-github
    to: https://github.com/nuxt/cli/blob/main/src/commands/module/
    size: xs
---

Nuxi provides a few utilities to work with [Nuxt modules](/modules) seamlessly.

## nuxi module add

```bash [Terminal]
npx nuxi module add <NAME>
```

Option        | Default          | Description
-------------------------|-----------------|------------------
`NAME` | - | The name of the module to install.
`--peerDeps, -p` | undefined | Installing peer dependencies.
`--devDeps, -D` | false | Use this with "-p" option. Enabling this option will install to devDependencies.

The command lets you install [Nuxt modules](/modules) in your application with no manual work.

When running the command, it will:
- install the module as a dependency using your package manager
- add it to your [package.json](/docs/guide/directory-structure/package) file
- update your [`nuxt.config`](/docs/guide/directory-structure/nuxt-config) file

**Example:**

Installing the [`Pinia`](/modules/pinia) module
```bash [Terminal]
npx nuxi module add pinia 
```

Installing the [`ESLint`](/modules/eslint) module and Installing the `eslint`
```bash [Terminal]
npx nuxi module add eslint -p eslint 
```

Installing the [`ESLint`](/modules/eslint) module and Installing the `eslint` in devDependencies
```bash [Terminal]
npx nuxi module add eslint -p eslint -D
```

Installing the [`test-utils`](/modules/test-utils) module and Installing related libraries in devDependencies
```bash [Terminal]
npx nuxi module add test-utils -p vitest -p @vue/test-utils -p happy-dom -p playwright-core -D
```

## nuxi module search

```bash [Terminal]
npx nuxi module search <QUERY>
```

Option        | Default          | Description
-------------------------|-----------------|------------------
`QUERY` | - | The name of the module to search for.

The command searches for Nuxt modules matching your query that are compatible with your Nuxt version.

**Example:**

```bash [Terminal]
npx nuxi module search pinia
```
