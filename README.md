# NASA Explorer

NASA Explorer is a front-end web project for exploring NASA imagery through an interactive interface and map experience.

It includes:

- A landing page with feature highlights and category cards
- An interactive exploration page powered by Leaflet
- Layer switching between multiple NASA GIBS datasets
- An about page describing the project and data source

## Tech Stack

- HTML5
- Tailwind CSS v4 (compiled from `src/input.css`)
- JavaScript (vanilla)
- Leaflet.js
- AOS (Animate On Scroll)
- Font Awesome

## Data Source

Map layers are fetched from NASA GIBS (Global Imagery Browse Services) WMTS endpoints:

- https://gibs.earthdata.nasa.gov/

Configured layers in the app:

- True Color
- Temperature
- Night Lights

## Project Structure

```
.
├─ index.html
├─ explorerPage.html
├─ about.html
├─ src/
│  └─ input.css
├─ dist/
│  └─ output.css
├─ img/
├─ wmts.xml
├─ wmts4326.xml
└─ package.json
```

## Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Build Tailwind CSS

```bash
npm run build:css
```

This script runs in watch mode and continuously writes styles to `dist/output.css`.

### 3. Open the project

You can open `index.html` directly in your browser, or use a local static server for the best experience.

Example with VS Code Live Server:

- Start Live Server from the project folder
- Visit the served URL for `index.html`

## Available Script

```bash
npm run build:css
```

- Compiles `src/input.css` into `dist/output.css`
- Watches for file changes

## Notes

- `explorerPage.html` initializes a Leaflet map and custom controls (zoom in/out, reset, and layer switching).
- The layer switch button cycles through predefined NASA imagery datasets.
- `wmts.xml` and `wmts4326.xml` are included for WMTS reference/capabilities context.

## License

This project currently does not define a custom license beyond the default package metadata. Add a `LICENSE` file if you plan to distribute it publicly.
