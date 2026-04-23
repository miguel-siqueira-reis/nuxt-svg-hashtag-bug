# Nuxt SVG Hashtag Bug

This repository reproduces a build error where the bundler confuses SVG fragment identifiers (`#`) with Nuxt Subpath Imports.

### Steps to reproduce:
1. `npm install`
2. `npm run build`

### Error:
`[commonjs--resolver] Missing "#" specifier in "nuxt" package`

### Cause:
The file `aoo/app.vue` contains an `<image href="#" />` which triggers the Vite/Rollup resolver incorrectly.
