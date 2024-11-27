# Atoms webpack.
Small atomic bits for crafting webpack configs.

```sh
npm i atoms_webpack
```

**webpack.config**
```js
const { rules, plugins, loaders } = require('atoms_webpack');

module.exports = {
  entry: './src/app.js',
  output: {
    /* ... */
  },

  module: {
    rules: [
      rules.js(),
      rules.images(),
      rules.css(),
    ]
  },

  plugins: [
    plugins.uglify(),
    plugins.loaderOptions(),
    plugins.extractText(),
  ]
}
```