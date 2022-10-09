

<h1>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/24266948/194764100-9283abd4-b312-480a-9c0e-b2dcbcf2c655.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/24266948/194763419-4860ef73-a02f-46f5-8a99-604426b45ecf.svg">
    <img alt="GitHub Octicons: Book" width="100" align="left" src="https://user-images.githubusercontent.com/24266948/194763419-4860ef73-a02f-46f5-8a99-604426b45ecf.svg">
  </picture>
  RABIT-DOCS
  <br />
</h1>
<span>
    <a href="LICENSE.md"><img alt="License Badge" src="https://img.shields.io/github/license/FIT3170-FY-Project-7/RABIT-DOCS?label=license&style=flat-square" /></a>
    &nbsp; <a alt="Build Workflow Status" href="https://github.com/FIT3170-FY-Project-7/RABIT-DOCS/actions/workflows/deploy.yml"><img src="https://img.shields.io/github/workflow/status/FIT3170-FY-Project-7/RABIT-DOCS/Deploy?style=flat-square" /></a>
    &nbsp; <a alt="GitHub Pages Workflow Status" href="https://github.com/FIT3170-FY-Project-7/RABIT-DOCS/actions/workflows/pages/pages-build-deployment"><img src="https://img.shields.io/github/workflow/status/FIT3170-FY-Project-7/RABIT-DOCS/pages%20build%20and%20deployment?label=github%20pages&style=flat-square" /></a>
</span><br><br>

_This repository contains the source code (and output pages) for RABIT documentation._

---

## Editing, Building, Local Deployment
  
1. Install mdBook by following the [installation guide](https://rust-lang.github.io/mdBook/guide/installation.html).
2. To add more pages, create a new .md file in the `src` folder, and add an entry in `SUMMARY.md`. See the [mdBook docs](https://rust-lang.github.io/mdBook/format/summary.html) for the syntax.
3. To build and see the output locally, run `mdbook serve` and go to http://localhost:3000.

## Production Deployment

- You cannot edit directly in main branch, so you'll need to create a new branch or fork the repo for non-collaborators.
- When you're ready, just create a pull request. Once merged, it will be built and deployed automatically to github pages.
- **Note: You should _NOT_ edit or branch from the `gh-pages` branch.**
