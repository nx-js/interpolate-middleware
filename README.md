# The interpolate middleware

The `interpolate` middleware is responsible for dynamic and one-time text interpolation from the state into the HTML view.

- name: interpolate
- middleware dependencies: [observe](https://github.com/nx-js/observe-middleware)
- all middleware dependencies: [observe](https://github.com/nx-js/observe-middleware)
- processes: text nodes
- throws on: nothing
- use as: content middleware
- [docs](http://nx-framework.com/docs/middlewares/interpolate)

## Installation

`npm install @nx-js/interpolate-middleware`

## Usage

```js
const component = require('@nx-js/core')
const observe = require('@nx-js/observe-middleware')
const interpolate = require('@nx-js/interpolate-middleware')

component()
  .useOnContent(observe)
  .useOnContent(interpolate)
  .register('interpolate-comp')
```

```html
<interpolate-comp>
  <p>${name} is ${age | unit 'year'} old</p>
</interpolate-comp>
```
