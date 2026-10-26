# Repository Guidelines

## Project Structure & Module Organization

This repository is a documentation-only catalog; it has no application source tree, build output, or automated test directory.

- `README.md` is the published macOS app directory and category index.
- `EDITORIAL_GUIDELINES.md` defines listing quality, ordering, and verification rules.
- `CONTRIBUTING.md` documents the public contribution process.
- `GIT_CONVENTION.md` defines commit and pull request conventions.
- `.github/ISSUE_TEMPLATE/` and `.github/PULL_REQUEST_TEMPLATE.md` contain GitHub forms.
- `assets/` is reserved for repository-owned brand assets.

## Build, Test & Validation Commands

There is no build system, package manager, test framework, or coverage target. Validate changes manually:

```sh
git diff --check
rg -n "^### " README.md
curl -I https://example.com
```

Use `git diff --check` for whitespace errors, inspect category headings with `rg`, and replace the example URL with every added official or **Read more** link. Preview Markdown on GitHub before merging and confirm that category links resolve to existing headings.

## Style & Naming Conventions

Use UTF-8, LF line endings, and a final newline, as configured in `.editorconfig` and `.gitattributes`. Preserve Markdown's two trailing spaces when they intentionally create a line break. Name new assets with descriptive lowercase kebab-case, such as `assets/project-logo.svg`.

Place each app in one primary category. Keep categories and app names alphabetical, omit empty categories, and update the category index when headings change. Write one neutral, independently sourced description of roughly 100–180 characters. Avoid marketing language, unsupported claims, pricing badges, screenshots, and third-party app icons.

## Testing Guidelines

Confirm that each app is public and maintained, its official URL works, and any `coolmac.app/apps/<slug>` page exists. Check for duplicates, accurate categorization, consistent entry formatting, and valid internal links.

## Commit & Pull Request Guidelines

Follow `GIT_CONVENTION.md`: `<type>(<scope>): <summary>`, with a required scope and imperative summary. Example: `docs(catalog): add Raycast to productivity`. Use the smallest accurate type and keep each commit to one logical change. Mark breaking changes with `!` and explain migration impact in the body.

Keep pull requests narrowly scoped. Explain what changed and why, link relevant issues, list verification performed, and complete the PR checklist. Include screenshots only when demonstrating a rendering problem.
