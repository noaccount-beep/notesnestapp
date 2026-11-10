# AGENTS.md

- Static site with no build step. Netlify publishes the `public/` directory (see `netlify.toml`).
- `public/index.html` holds all markup, styles (inline `<style>`) and behaviour (inline `<script>`). The product catalogue is the `data` array in that script.
- The basket, the payment modal and the owner/admin view run in the browser only. Nothing is saved, and no payment provider is connected yet.
- Keep the site dependency-free unless a feature needs a backend. For storage, use Netlify primitives (Netlify Database or Netlify Blobs). For forms, use Netlify Forms.
