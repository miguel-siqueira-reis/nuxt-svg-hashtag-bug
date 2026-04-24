# Nuxt SVG Hashtag Bug

⚠️ **STATUS: RESOLVED / UPSTREAM BUG**
This issue has been identified as a bug in the Vue.js Core compiler.
A fix has been proposed here: [vuejs/core#14756](https://github.com/vuejs/core/pull/14756)

---

## Overview:
This repository reproduces a build error where the bundler confuses SVG fragment identifiers (`#`) with Nuxt Subpath Imports.

### Steps to reproduce:
1. `npm install`
2. `npm run build`

### Error:
`[commonjs--resolver] Missing "#" specifier in "nuxt" package`

### Cause:
The file `app/app.vue` contains an `<image href="#" />` which triggers the Vite/Rollup resolver incorrectly.
