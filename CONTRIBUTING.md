# Contributing

Thanks for taking the time to contribute. This repository is small, so the
process is light, but every change follows the same loop.

## Workflow

1. **Open an issue** describing the problem or the change you want to make.
2. **Create a branch** from `main` using a prefix that matches the change:
   - `feat/` new functionality
   - `fix/` bug fixes
   - `docs/` documentation only
   - `chore/` tooling, config, housekeeping
   - `ci/` CI workflows
3. **Commit** small, focused changes (see below).
4. **Open a pull request** against `main`. Put `Closes #<issue>` in the
   description so the issue closes automatically on merge.
5. **Wait for CI** to pass, then merge.

## Commit messages

- Use the imperative mood in the subject: "Add license", not "Added license".
- Keep the subject under about 72 characters, no trailing period.
- Use the body to explain *why* when it is not obvious from the diff.
- Reference the issue in the body, for example `Refs #12`.

## Pull requests

- One logical change per PR.
- Fill in the PR template: what changed, why, and how it was checked.
- Do not force-push to `main`, and do not rewrite shared history.

## Reporting bugs and asking questions

- Bugs and feature requests: use the issue templates.
- Questions: use GitHub Discussions (Q&A category) once it is enabled.

## License

By contributing, you agree that your contributions are licensed under the
[MIT License](LICENSE).
