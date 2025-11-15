# lefthook
A collection of lefthook configs for common development workflows

## Features

This repository provides pre-configured lefthook configurations for various Git hooks and package managers.

### Commit Message Hooks

#### pnpm
- **commitlint** (`configs/commit-msg/pnpm/commitlint.yml`) - Validates commit messages using commitlint to ensure they follow conventional commit standards

### Pre-Commit Hooks

#### pnpm
- **fmt** (`configs/pre-commit/pnpm/fmt.yml`) - Formats staged files using Prettier
- **lint** (`configs/pre-commit/pnpm/lint.yml`) - Lints staged files using ESLint with auto-fix
- **lint-fmt** (`configs/pre-commit/pnpm/lint-fmt.yml`) - Runs both ESLint and Prettier on staged files
- **nxsync** (`configs/pre-commit/pnpm/nxsync.yml`) - Syncs Nx workspace configuration
- **nxsync-lint-fmt** (`configs/pre-commit/pnpm/nxsync-lint-fmt.yml`) - Full workflow: syncs Nx workspace, then runs ESLint and Prettier

## Usage

To use any of these configurations, reference them in your `lefthook.yml` file using the `remotes` directive:

```yaml
remotes:
  - git_url: https://github.com/dcdavidev/lefthook
    configs:
      - configs/commit-msg/pnpm/commitlint.yml
```

Or copy the configuration content directly into your `lefthook.yml` file.

---

## License

This project is licensed under the MIT License.

**Copyright (c) 2025 Davide Di Criscito**

For the full details, see the [LICENSE](LICENSE) file.
