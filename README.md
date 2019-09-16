# vue-esm-types

Simple recreation of a problem where Vue.js alternate builds (such as the ESM
build) don’t properly expose types to TypeScript.

To recreate, run:

```bash
npm i
npm run build
```

You should see the following error:

```
Could not find a declaration file for module 'vue/dist/vue.esm.browser'. '../node_modules/vue/dist/vue.esm.browser.js' implicitly has an 'any' type.
  Try `npm install @types/vue` if it exists or add a new declaration (.d.ts) file containing `declare module 'vue/dist/vue.esm.browser';`
```

Try swapping out the import with the commented-out one, and it will build
perfectly.
