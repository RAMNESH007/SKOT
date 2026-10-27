# SKOT OS — Sky Over Transmission

A static deployment clone of **https://skot-os.vercel.app/**, captured on 27 October 2026. This is the airspace operations simulator. It is not a clone of the separate officialskot marketing website.

## What this repository contains

The deployed HTML, JavaScript and CSS are preserved byte-for-byte in `public/`. This keeps the simulation interface and client-side behavior present in the captured deployment. The JavaScript is the compiled production bundle, not recovered React/TypeScript component source. Original source files, build configuration, server code and Git history were not available from the live URL.

Small dependency-free Node scripts provide local serving and static build packaging. No npm dependencies or API keys are required by these scripts.

## Run locally

Install Node.js 20 or newer, open this directory in a terminal, and run:

```sh
npm start
```

Open http://localhost:3000. Internet access is needed for the external services below. Do not open `index.html` directly using a file URL.

For a deployment build:

```sh
npm run build
npm run preview
```

The output is `dist/`. Stop the first server before running preview on the same port, or set `PORT` to another port.

## Clone this repository

```sh
git clone https://github.com/RAMNESH007/SKOT.git
cd SKOT
npm start
```

Open http://localhost:3000. The `main` branch contains the captured simulator and local setup.

## Deploy on Vercel

Import the GitHub repository into Vercel. Use the Other framework preset, build command `npm run build`, and output directory `dist`. These values are also specified in `vercel.json`. This creates a separate deployment; it does not modify the original website.

## External services

The captured app references:

- Google Fonts for Inter and JetBrains Mono.
- MapLibre GL 4.7.1 CSS on unpkg; MapLibre JavaScript is in the application bundle.
- CARTO/OpenStreetMap-based dark map tiles.
- Esri World Imagery and boundary/label tiles.
- The public OSRM routing endpoint for road geometry.

Availability, usage limits and terms of those providers apply. This is not an offline copy of map data. Map and route availability can differ by network. The clone does not add a backend or real aircraft control, and simulation behavior is not evidence of operational flight-safety capability.

## Editing and provenance

Edit `public/index.html` or CSS for small changes. For maintainable feature development, obtain the original component source and replace the compiled snapshot with its build pipeline. No top-level open-source license is asserted for the captured app. Existing third-party notices in the bundle are retained; original authors' rights remain unchanged.

`snapshot.json` records the capture URL and SHA-256 hashes so the deployed assets can be checked against this snapshot.
