# SvelteKit PWA Starter

> 🚨 WIP. I've only tested on iOS Safari, and it does not include service worker/caching/offline functionality (yet).

A bare-minimum starter repository for a SvelteKit progressive web app (PWA) that's installable to a device's home screen. It's currrently just the SvelteKit skeleton project starter, with the [following additions]('https://github.com/evanwinter/sveltekit-pwa-starter/commit/80fbd15ac79b71867eda6dd48e3b1d9fcca2dda2'):

- Adds `/static/manifest.json`
- Adds an icon, in two sizes: `/static/icon-192x192.png` and `/static/icon-512x512.png`.
- Adds `<meta>` tags in `/src/app.html`:

```html
<link rel="manifest" href="/manifest.json" />
<meta name="theme-color" media="(prefers-color-scheme: light)" content="white" />
<meta name="theme-color" media="(prefers-color-scheme: dark)" content="black" />
```

These additions make the application installable to your device's home screen.

## Developing

Install dependencies with `npm install` (or `pnpm install` or `yarn`), and start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
