# P6 Clones Timing - Alt1 Plugin

A RuneScape 3 Alt1 plugin boilerplate built with TypeScript and Webpack.

## Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher recommended)
- [Alt1 Toolkit](https://runeapps.org/alt1) installed

## Installation

`alt1://addapp/https://nullopt.github.io/appconfig.json`

```bash
npm install
```

## Development

### Build for production
```bash
npm run build
```


### Watch mode (auto-rebuild on changes)
```bash
npm run watch
```

### Development server with hot reload
```bash
npm run dev
```

`alt1://addapp/http://localhost:8080/appconfig.json`

## Adding to Alt1

1. Build the project: `npm run build`
2. Host the `dist/` folder on a web server (local or remote)
3. In Alt1, open the browser and navigate to your hosted URL
4. Alt1 will detect the `appconfig.json` and offer to add the app

### Local Development

For local development, you can use the webpack dev server:

```bash
npm run dev
```

Then add `http://localhost:8080` to Alt1.

## Project Structure

```
├── src/
│   ├── index.ts          # main plugin entry point
│   ├── index.html        # HTML template
│   ├── style.css         # plugin styles
│   └── appconfig.json    # Alt1 app configuration
├── dist/                 # build output (generated)
├── package.json
├── tsconfig.json
└── webpack.config.js
```

## Alt1 API Usage

The plugin uses the `alt1/base` module for screen capture and image detection:

```typescript
import * as a1lib from "alt1/base";

// check if Alt1 is available
if (a1lib.hasAlt1) {
  // capture the game screen
  const img = a1lib.captureHoldFullRs();
  
  // convert to ImageData for processing
  const imageData = img.toData();
}
```

## Available Alt1 Modules

- `alt1/base` - Core functionality, screen capture, image detection
- `alt1/ocr` - Text recognition
- `alt1/chatbox` - Chatbox reading
- `alt1/buffs` - Buff bar detection
- `alt1/tooltip` - Tooltip reading

## Configuration

Edit `src/appconfig.json` to customize your app:

```json
{
  "appName": "Your App Name",
  "description": "Your app description",
  "appUrl": "index.html",
  "configUrl": "appconfig.json",
  "permissions": ["pixel", "overlay"]
}
```

### Permissions

- `pixel` - Required for screen capture
- `overlay` - Required for drawing overlays on the game

## Resources

- [Alt1 GitHub](https://github.com/skillbert/alt1)
- [Alt1 Minimal Example](https://github.com/skillbert/alt1minimal)
- [RuneApps](https://runeapps.org/)

