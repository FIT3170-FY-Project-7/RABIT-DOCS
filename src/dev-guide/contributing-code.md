# Contributing code

## Branching rules

### Frontend and backend repositories

The following rules apply for the [RABIT-FRONTEND](https://github.com/FIT3170-FY-Project-7/RABIT-FRONTEND) and [RABIT-BACKEND](https://github.com/FIT3170-FY-Project-7/RABIT-BACKEND).

Several branches exist in these repositories:

- The `main` branch is where a stable version of the app exists. If you're a user, you want to build RABIT from this branch.
- The `dev` branch is where all changes that are slated for the next branch resides. This branch contains the latest features and improvements but may contain bugs or regressions as the codebase has not been thoroughly tested. **All feature and development branches should be made from this branch.**
- Branches with `feature/` prefix contains in-progress work relating to new features and enhancements. Feature names should be concise and descriptive and in kebab case, for example `feature/plot-sharing`.
- Branches with `issue/` prefix contains in-progress work relating to a bug. The issue name should be a concise description of what the issue is about (e.g. `issue/broken-build`).

Once the work on the feature or issue branch is complete, they will be merged to the `dev` branch. When a new version is ready to be released, the latest commit from `dev` will be merged to the `main` branch.

## Common repository

The convention for [RABIT-COMMON](https://github.com/FIT3170-FY-Project-7/RABIT-COMMON) is similar to the one above. However, there is no stable branch here, with the `main` branch acting as `dev` branch where all feature and development branches are based on.

## Contribution workflow

1. Decide on where the code should go
   - If your contribution spans both frontend and backend, then you will need to do the next steps for each repository.
2. Create a new branch from `dev` (frontend and backend) or `main` (common)
   - If you don't have push access to the repositories, you may need to fork the repository first.
3. Work on the branch
4. Create a pull request
   - Follow the instructions given in the provided template
   - Frontend and backend: make sure to set `dev` as the base branch
5. Wait until one of our maintainers approved your PR
6. Your changes should be up in the `dev`/`main` branch! 🥳

## Coding convention
