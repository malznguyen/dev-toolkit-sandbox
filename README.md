# dev-toolkit-sandbox

[![CI](https://github.com/malznguyen/dev-toolkit-sandbox/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/malznguyen/dev-toolkit-sandbox/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A public sandbox for practicing a clean GitHub workflow end to end:
issue → branch → pull request → CI → merge.

Every change in this repository goes through that loop, so the history
doubles as a worked example of how a small project is set up properly:
license, ignore rules, contribution guide, issue and PR templates, and
continuous integration.

## What's inside

| Path | Purpose |
| --- | --- |
| [`LICENSE`](LICENSE) | MIT license |
| [`.gitignore`](.gitignore) | OS, editor, secret and build-output ignore rules |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Branch naming, commit style, PR flow |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | Bug report and feature request forms |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | What / why / how-checked PR template |
| [`.github/workflows/ci.yml`](.github/workflows/ci.yml) | CI: markdownlint + yamllint |
| [`.markdownlint.jsonc`](.markdownlint.jsonc), [`.yamllint.yml`](.yamllint.yml) | Linter configuration |

## Usage

### Reuse the scaffolding in another project

Copy the files you need into your own repository, for example:

```sh
git clone https://github.com/malznguyen/dev-toolkit-sandbox.git
cp -r dev-toolkit-sandbox/.github \
      dev-toolkit-sandbox/.gitignore \
      dev-toolkit-sandbox/.markdownlint.jsonc \
      dev-toolkit-sandbox/.yamllint.yml \
      path/to/your-project/
```

Then update the Discussions link in `.github/ISSUE_TEMPLATE/config.yml`
and the copyright line in `LICENSE`.

### Run the linters locally

The same checks that CI runs:

```sh
# Markdown (needs Node.js)
npx --yes markdownlint-cli2 "**/*.md" ".github/**/*.md"

# YAML (needs Python)
pip install yamllint
yamllint --strict .
```

### Make a change

1. Open an issue describing the change.
2. Branch from `main` (`feat/`, `fix/`, `docs/`, `chore/`, `ci/`).
3. Open a pull request with `Closes #<issue>` in the description.
4. Merge once CI is green.

Details are in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE) © 2026 Nguyen Hoang Ha
