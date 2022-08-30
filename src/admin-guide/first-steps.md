# First steps

## Clone the repositories


Clone the RABIT repository and all submodules.

```
git clone https://github.com/FIT3170-FY-Project-7/RABIT-COMMON.git --recursive
```

## Switch branch

Switch to the `dev` branch in both `RABIT-FRONTEND` and `RABIT-BACKEND` or any branch that you're currently working on.
**Do not use the `main` branch** since they don't contain anything at the moment. This may change in the future.

## Set up Firebase

We use [Firebase Auth](https://firebase.google.com/docs/auth) for our authentication system. You need to set up a
Firebase project and registering an app by following step 1 of [this guide](https://firebase.google.com/docs/web/setup).

## Next steps

Proceed to either [Docker](./docker.md) or [manual install](./manual-install.md) pages, depending on your deployment
method.
