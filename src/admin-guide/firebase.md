# Firebase

RABIT currently do not have a proper authentication system, and all plots and data are stored under a single temporary user. However, a framework for user management using Firebase exists in the codebase but is disabled by default. This page shows you how you can use them for testing purposes. Please note that this step is optional, and the app will run just fine without Firebase.

## Set up Firebase

We use [Firebase Auth](https://firebase.google.com/docs/auth) for our authentication system. You need to set up a
Firebase project and registering an app by following step 1 of [this guide](https://firebase.google.com/docs/web/setup).

## Add Firebase environment variables

In the `.env` file in In `RABIT-BACKEND`, go to your project settings and scroll down to the app you just registered. Then fill out the
variables as follows:

```shell
USE_FIREBASE=1
FIREBASE_API_KEY="" # firebaseConfig.apiKey
FIREBASE_AUTH_DOMAIN="" # firebaseConfig.authDomain
FIREBASE_PROJECT_ID="" # firebaseConfig.projectId
FIREBASE_STORAGE_BUCKET="" # firebaseConfig.storageBucket
FIREBASE_MESSAGING_SENDER_ID="" # firebaseConfig.messagingSenderId
FIREBASE_APP_ID="" # firebaseConfig.appId
```

## Next steps

Proceed to the next steps for either [Docker](./docker.md) or [manual install](./manual-install.md) pages, depending on your deployment method.
