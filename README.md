# ChaufX Mobile

Customer and driver mobile apps for ChaufX Canada.

This repository contains:

- customer mobile app
- driver mobile app
- shared mobile config, types, and UI packages

## Tech stack

- Expo
- React Native
- TypeScript
- Mapbox

## Repository structure

```text
apps/customer-mobile
apps/driver-mobile
packages/config
packages/types
packages/ui
```

## Environment variables

Copy the example file for each app:

```bash
cp apps/customer-mobile/.env.example apps/customer-mobile/.env
cp apps/driver-mobile/.env.example apps/driver-mobile/.env
```

Set:

```env
EXPO_PUBLIC_API_URL=http://localhost:4000/api
EXPO_PUBLIC_MAPBOX_TOKEN=pk.your_public_mapbox_token
```

For production builds, replace `EXPO_PUBLIC_API_URL` with your deployed backend URL.

## Install

From the repository root:

```bash
npm install
```

## Run customer app

```bash
npm run dev:customer
```

## Run driver app

```bash
npm run dev:driver
```

## Native builds

Customer:

```bash
npm run ios:customer
npm run android:customer
```

Driver:

```bash
npm run ios:driver
npm run android:driver
```

## Important note about Mapbox

These apps use `@rnmapbox/maps`, so Expo Go is not enough for full map testing.
Use a development build or native run commands.

## Notes

- This repo is intentionally mobile-only.
- The web app lives in `ChaufX-Web`.
- The API lives in `ChaufX-backend`.
