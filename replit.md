# Watts & Drops

A Vue.js resource monitoring dashboard for tracking electricity and water usage.

## Overview

This is a frontend-only Vue.js application built with:
- Vue 3
- Vite 7 (build tool and dev server)
- Tailwind CSS 4

## Project Structure

```
/
├── index.html          # Entry HTML file
├── src/
│   ├── main.js         # Vue app entry point
│   ├── App.vue         # Root component
│   └── style.css       # Global styles
├── public/             # Static assets
├── package.json        # Dependencies and scripts
└── vite.config.js      # Vite configuration
```

## Development

The dev server runs on port 5000 with host `0.0.0.0` to allow Replit's proxy access.

### Scripts
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## Deployment

Configured as a static deployment with:
- Build command: `npm run build`
- Public directory: `dist`
