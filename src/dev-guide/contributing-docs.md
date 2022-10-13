# Contributing documentation

The documentation is written as a collection of markdown files, which are then converted to a website using [mdbook](https://rust-lang.github.io/mdBook/).

## Branching rules

- The `main` branch is where the [current version of the documentation](https://fit3170-fy-project-7.github.io/RABIT-DOCS/) is built from. All development branches should be based on this branch.
- Branches with `pages/` prefix contains in-progress work on specific page or section. For example, improvements to the user guide has the name of `pages/user-guide`.
- Branches with `issue/` prefix contains in-progress work relating to a bug. This could be typos, grammar and writing style or deployment issues.
- The `gh-pages` branch contains the compiled site files built from `main` branch. This branch is automatically built using a GitHub action, and they should not be modified or branched from.

## File structure

### `book.toml`

This file contains the configuration for mdbook. You shouldn't need to change anything here.

### `src`

This directory contains all source markdown files, images, code or any files that will be included in the compiled site.

### `src/SUMMARY.md`

This file creates the table of contents that you see in the sidebar. See the [mdbook documentation](https://rust-lang.github.io/mdBook/format/summary.html) for its syntax.

### `book` (local build only)

This directory is automatically generated using [mdbook's build commands](https://rust-lang.github.io/mdBook/cli/index.html). It contains the site's build artefacts.

### Other

- `src/images` contains all images of the site.
- `src/code` contains all code files that is included in the documentation using the [`{{#include}}` directive](https://rust-lang.github.io/mdBook/format/mdbook.html#including-files). This folder does not exist at the moment, so feel free to create one if you need to.

## Contribution workflow

1. Create a branch from `main`
   - If you don't have push access to the repositories (which, unless you're a maintainer you likely won't), you may need to fork the repository first.
2. Read and understand the build process outlined in the ["Editing, Building, Local Deployment" section of README](https://github.com/FIT3170-FY-Project-7/RABIT-DOCS#editing-building-local-deployment)
3. Work on the branch
4. Create a pull request
   - Follow the instructions given in the provided template
5. Wait until one of our maintainers approved your PR and merge it to `main`
6. The site will be rebuilt, and your changes will be published.
