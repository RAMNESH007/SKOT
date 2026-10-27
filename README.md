# SKOT OS — Sky Over Transmission

**Low-altitude airspace coordination, planning and simulation.**

SKOT explores how existing ground infrastructure—roads, railways, rivers, canals and utility corridors—can provide a foundation for structured virtual aerial routes. Its goal is to support coordinated airspace for emergency response, autonomous delivery and future aerial mobility.

> We do not build new infrastructure. We unlock existing infrastructure.

[Launch SKOT OS](https://skot-os.vercel.app/) · [Project repository](https://github.com/RAMNESH007/SKOT)

## Application

This repository contains the SKOT OS browser simulation, application assets, local server and deployment configuration. The interface supports exploring mapped operations, simulated aircraft, incidents and session reports. It runs in the browser, with online map and routing services supplying geographic context.

The current application is a simulation environment. Operational aircraft integration and live flight control are outside this release.

## Getting started

Requirements: Node.js 20 or newer and an internet connection for map, routing and font services.

Download the project using GitHub's **Code → Download ZIP**, extract it, and open a terminal in the project folder. Run:

```sh
npm start
```

Open [localhost:3000](http://localhost:3000). The local server and build scripts use Node.js built-in modules and require no package installation.

| Command | Purpose |
| --- | --- |
| `npm start` | Serve the application locally |
| `npm run dev` | Serve the application from `public/` |
| `npm run build` | Prepare deployment files in `dist/` |
| `npm run preview` | Serve the prepared `dist/` directory |

Stop the running server before starting another on the same port. Set the `PORT` environment variable to use a different port.

## Project structure

| Path | Contents |
| --- | --- |
| `public/index.html` | Application entry page |
| `public/assets/` | Compiled application JavaScript and styles |
| `scripts/serve.mjs` | Local HTTP server |
| `scripts/build.mjs` | Static deployment packaging |
| `vercel.json` | Vercel build and output settings |
| `asset-manifest.json` | SHA-256 checksums for application assets |
| `VALIDATION.md` | Completed checks and verification status |

The build command packages the application assets in `public/` into `dist/`.

## Deployment

Import **RAMNESH007/SKOT** into Vercel with these settings:

| Setting | Value |
| --- | --- |
| Framework preset | Other |
| Build command | `npm run build` |
| Output directory | `dist` |

These build settings are included in `vercel.json`. The `dist/` directory can also be served by a static web host.

## Technology and services

- React-based browser interface and MapLibre GL map rendering.
- Node.js for local serving and deployment packaging.
- CARTO/OpenStreetMap-based dark map tiles.
- Esri imagery and geographic labels.
- OSRM road-route geometry.
- Inter and JetBrains Mono through Google Fonts.

External services require network access and remain subject to their providers' availability and terms. Third-party library notices and map attribution are retained.

## Contact

[officialskot.org@gmail.com](mailto:officialskot.org@gmail.com)
