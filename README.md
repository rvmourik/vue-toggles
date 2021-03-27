<h1 align="center">Vue Toggles</h1>
<p align="center">
A highly customizable and accessible toggle.
Now with SSR support!
</p>

<p align="center">
<a href="https://www.npmjs.com/package/vue-toggles"><img src="https://img.shields.io/npm/v/vue-toggles.svg?style=flat-square"/> <img src="https://img.shields.io/npm/dt/vue-toggles.svg?style=flat-square"/></a> <a href="https://vuejs.org/"><img src="https://img.shields.io/badge/vue-2.x-brightgreen.svg?style=flat-square"/></a>
</p>

<p align="center">
<img src="./vue-toggles.jpg" alt="Vue Toggles Logo"/>
</p>

## Demo

- [Demo](https://vue-toggles.netlify.app/)
- [CodeSandbox](https://codesandbox.io/s/vue-toggles-mkkp4?file=/src/App.vue)

## Introduction

Vue Toggles comes out of the box with accessibility support for:

- `aria-checked` depending on state
- `aria-readonly` if the toggle is disabled
- `prefers-reduced-motion` if the user has requested any type of motion reduction [[prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)]

### Accessibility

What's left for you, when it comes to accessibility, is labeling the toggle correctly. This is either done by:

- A `<label for="example-id">Toggle description</label>` followed by the toggle component `<VueToggles id="example-id" />`
- An `aria-label`, for example `<VueToggles aria-label="Toggle description" />`. Remember, you still need a visual text description of what the toggle does

The `focus`-style is also left up to you — which is recommended you don't remove. If you think the default is ugly, style it yourself!

## Installation

```
npm i vue-toggles
```

### Import

```javascript
import Vue from 'vue';
import VueToggles from 'vue-toggles';

Vue.component('VueToggles', VueToggles);
```

### SSR import (Nuxt for example)

```javascript
import Vue from 'vue';
import VueToggles from 'vue-toggles/dist/vue-toggles.ssr';
import 'vue-toggles/dist/vue-toggles.ssr.css';

Vue.component('VueToggles', VueToggles);
```

## Usage

The toggle is very easy to use out of the box. The bare minimum for it to work is a `@click`-function and a `:value`-prop.

```html
<VueToggles :value="value" @click="value = !value" />
```

## Options

You can also add more props to customize things like color and width/height.

```html
<VueToggles
  height="30"
  width="90"
  checkedText="On"
  uncheckedText="Off"
  checkedBg="#b4d455"
  uncheckedBg="lightgrey"
  :value="value"
  @click="value = !value"
/>
```

## Properties

| Name           | Type             | Default   | Description                                       |
| -------------- | ---------------- | --------- | ------------------------------------------------- |
| value          | Boolean          | `false`   | Initial state of the toggle button                |
| disabled       | Boolean          | `false`   | Toggle does not react on mouse or keyboard events |
| reverse        | Boolean          | `false`   | Reverse toggle to Right to Left                   |
| height         | [String, Number] | `25`      | Height of the toggle in `px`                      |
| width          | [String, Number] | `75`      | Width of the toggle in `px`                       |
| checkedText    | String           | `null`    | Optional text when the toggle is checked          |
| uncheckedText  | String           | `null`    | Optional text when the toggle is unchecked        |
| checkedBg      | String           | `#5850ec` | Background color when the toggle is checked       |
| uncheckedBg    | String           | `#939393` | Background color when the toggle is unchecked     |
| checkedColor   | String           | `#ffffff` | Text color when the toggle is checked             |
| uncheckedColor | String           | `#ffffff` | Text color when the toggle is unchecked           |
| dotColor       | String           | `#ffffff` | Color of the toggle dot                           |
| fontSize       | [String, Number] | `12`      | Font size in `px`                                 |
| fontWeight     | [Number, String] | `normal`  | Font weight                                       |

### Browser compatibility

- Chrome: 40+
- Firefox: 25+
- Safari: 10+
- IE: 11+

### License

[MIT](http://opensource.org/licenses/MIT)
