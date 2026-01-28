# Watts & Drops

A College Resource Monitoring System built with Vue 3 + Vite + Tailwind CSS.

## Overview

This is a resource monitoring dashboard application that allows tracking of resource consumption (electricity, water, etc.) in college facilities. Users can view and report issues with resources like projectors, electricity, and other infrastructure.

## Project Structure

- `/src` - Vue 3 source code
  - `/src/main.js` - Application entry point
- `/public` - Static assets
- `/index.html` - HTML entry point
- `/vite.config.js` - Vite configuration

## Tech Stack

- **Framework**: Vue 3
- **Build Tool**: Vite 7.x
- **Styling**: Tailwind CSS 4.x
- **Language**: JavaScript (ES Modules)

## Development

Run the development server:
```bash
npm run dev
```

The server runs on `http://0.0.0.0:5000` with all hosts allowed for Replit compatibility.

## Build

Build for production:
```bash
npm run build
```

Output is placed in the `dist` directory.

## Deployment

Configured for static deployment with Vite build output served from the `dist` directory.
