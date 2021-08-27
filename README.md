# ts-tooling [![Lint](https://github.com/asjadanis/ts-tooling/actions/workflows/lint.yml/badge.svg)](https://github.com/asjadanis/ts-tooling/actions/workflows/lint.yml)

A very simple and extendable boilerplate for typescript configured with ESLint, Prettier, Husky, Commitizen.

### Lint

To modify eslint rules update your `.eslintrc` file in the project root, it currently uses 
- "eslint:recommended",
- "plugin:@typescript-eslint/recommended",

To lint the entire project run

```bash
yarn lint
```

### Prettier

To update prettier rules modify `.prettierrc` file in the root of repo.

To format the entire project run

```bash
yarn format
```

### Conventional Commits

[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) are supported using [commitizen](https://github.com/commitizen/cz-cli)

To use commitizen with your commits run

```bash
yarn cz
````

### Husky

A `pre-commit` hook is setup using husky and and it will run lint and format command on all staged files that match the target files (src/**/*.ts)

```bash
#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

npx lint-staged
```

