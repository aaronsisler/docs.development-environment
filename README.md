# docs.development-environment

## Purpose Of This Repo

## What A Section Should Contain

- Header
- Language Versioner
  - What manages the version of the language "versioner" e.g. Brew manages NVM, SDK Man is self updating.
- Language Version
  - What manages the version of language e.g. NVM for NodeJs, SDK Man for Java, etc.
- Install & Build Tool
  - What install/build tool is used per language e.g. gradle for Java, yarn for NodeJs

## Languages

- [Java](./languages/java.md)
- [Node.js](./languages/node-js.md)

## Python

| Language Versioner | .zshrc Needed | Language Version | Alias Neede | Install & Build Tool |
| ------------------ | ------------- | ---------------- | ----------- | -------------------- |
| Brew               | No            | Brew             | Yes         | pipenv               |

## TODO

### File names to look into what tech they are from next-enterprise

- .all-contributorsrc
  - npm dev package that puts information into this file
- .eslintrc.js
  - Has some nice plugins and auto sorting/saving
  - .eslintignore
    - Folders to ignore i.e. node_modules, etc.
- .pre-commit-config.yaml
  - Requires the brew package `pre-commit`
  - References a repo that seems to have the "default" rules
  - https://pre-commit.com/
- git-conventional-commits.yaml
- .releaserc

  - Uses npm semantic-release
  - This is used in tandem with the git conventional commits plugin to figure out how to version the release given what was added/removed
  - https://semantic-release.gitbook.io/semantic-release/usage/installation

- env.mjs
  - @t3-oss/env-nextjs
  - createEnv
- instrumentation.ts
  - @vercel/otel
  - https://nextjs.org/docs/pages/building-your-application/optimizing/open-telemetry
- jest.config.ts
- next-env.d.ts
  - https://nextjs.org/docs/basic-features/typescript
- next.config.mjs
  - https://nextjs.org/docs/pages/api-reference/next-config-js
- playwright.config.ts
- postcss.config.js
- prettier.config.ts
  - prettierignore
- renovate.json
- reset.d.ts
- tailwind.config.js
- tsconfig.json
- storybook

### Things to understand

- .mjs file types
  - This is related to the import/export .mjs compared to require/module.exports .cjs
- Folder and file structure
  - https://nextjs.org/docs/getting-started/project-structure
  - https://dev.to/vadorequest/a-2021-guide-about-structuring-your-next-js-project-in-a-flexible-and-efficient-way-472
- What the GHA files are doing
