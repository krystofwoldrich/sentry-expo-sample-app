# sentry-expo-sample-app

This is simple app example to show how sentry-expo works step by step, look into the commits.

## How this app was created?

The process is simple, create initial app, install `sentry-expo` and additional modules. Then add `Sentry.init` to your app and if you want source maps add `postPublishHook`.

```bash
npx create-expo-app sentry-expo-sample-app

npx expo install sentry-expo
npx expo install expo-application expo-constants expo-device expo-updates @sentry/react-native
```

## How to build the app locally

We are using `eas-cli`. To build `apk` that we can install to our simulator add `preview` in `eas.json`.

```bash
yarn global add eas-cli
eas login
eas build:configure
eas build --platform android --local --profile preview
# eas build --platform ios --local --profile preview
```
## How to build in Expo

```bash
eas build -p android --profile preview
# eas build -p ios --profile preview
```
