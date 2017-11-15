# Getting Started

**uiv** is a Bootstrap 3 component lib implemented by Vue 2.

* **Lightweight**: ~17KB Gziped, Dependencies only Vue & Bootstrap CSS
* **SSR** (server-side rendering) supported.
* ES6 / CommonJS / AMD / Browser supported.

## Install

If you are using module bundlers such as Webpack, you can directly include package into your project via:

**NPM**:

```bash
$ npm install uiv --save
```

or **Yarn**:

```bash
$ yarn add uiv
```

Then register uiv components and directives all at once in your app's entry:

```javascript
// main.js
import 'bootstrap/dist/css/bootstrap.min.css'

import Vue from 'vue'
import * as uiv from 'uiv'

Vue.use(uiv)
```

That's it. Happy coding!

### No Conflict

All components & directives will be installed with no prefix by default, you can add any prefix to them to avoid conflicts with other libs if needed.

For example:

```javascript
Vue.use(uiv, {prefix: 'uiv'})
```

Results in:

* Components such as `<alert>` becomes `<uiv-alert>`
* Directives such as `v-tooltip` becomes `v-uiv-tooltip`
* Vue prototype methods such as `$alert` becomes `$uiv_alert`

## Import Individually

If you don't want all of the components for some reason (e.g. to save the bundle size), you can also import them individually.

### Example

```javascript
import { Alert } from 'uiv'

new Vue({
  components: {
    Alert
  }
})
```

## Browsers

You can load & install uiv package directly in browsers.

### Example

```html
<!-- Remember to import Vue and Bootstrap CSS file before this! -->
<script src="//unpkg.com/uiv/dist/uiv.min.js"></script>
```

This will simply load the latest `uiv.min.js` into your page. For detail usages, you can visit [https://unpkg.com](https://unpkg.com).

### Complete Usage Example

```html
<!-- index.html -->
<html>
<head>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
  <script type="text/javascript" src="//vuejs.org/js/vue.min.js"></script>
  <script type="text/javascript" src="//unpkg.com/uiv/dist/uiv.min.js"></script>
</head>
<body>
<div id="app">
  <tabs>
    <tab>Tab content 1.</tab>
    <tab>Tab content 2.</tab>
  </tabs>
</div>
<script>
  // No need to install uiv, we already do this for you after script loaded.
  new Vue().$mount('#app')
</script>
</body>
</html>
```

This will create a working **Tabs** component on your page.

## Browser Compatibility

All browsers supported by [Vue 2](https://github.com/vuejs/vue) and [Bootstrap 3 CSS](https://github.com/twbs/bootstrap) are suppose to be also supported by this lib  (IE8 and below are not supported).
