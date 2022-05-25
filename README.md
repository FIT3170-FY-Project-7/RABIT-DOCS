# rabit-user-docs

This repository contains the source code (and output pages) for RABIT user documentation.

## Editing, building and deploying locally

1. Install mdbook by following the [installation guide](https://rust-lang.github.io/mdBook/guide/installation.html)
2. To add more pages, create a new .md file in the `src` folder, and add an entry in `SUMMARY.md`. See the [mdbook docs](https://rust-lang.github.io/mdBook/format/summary.html) for the syntax.
3. To build and see the output locally, run `mdbook serve` and go to http://localhost:3000.


## Deploying to prod

You cannot edit directly in main branch, so you'll need to create a new branch or fork the repo for non-collaborators.

When you're ready, just create a pull request. Once merged, it will be built and deployed automatically to github pages.

**You should NOT edit or branch off of `gh-pages` branch.**