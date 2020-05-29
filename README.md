<h3 align="center" style="margin: 30px 0 35px;">vuejs-fragment</h3>
<p align="center">
  <a href="https://www.npmjs.com/package/vuejs-fragment"><img alt="npm" src="https://img.shields.io/npm/v/vuejs-fragment"></a>
  <a href="https://travis-ci.org/AngusYang9/vuejs-fragment"><img src="https://travis-ci.org/AngusYang9/vuejs-fragment.svg?branch=master" /></a>
</p>

---

**vue.js fragment component.**


## 介绍
Fragment 是一个抽象组件，如果你想返回多个 DOM 元素，并且不想使用无用的容器元素包裹它们，fragment 为此设计。

## 为什么会有 fragment ?
 vue 组件的根元素必须是一个单独 DOM 节点，由于这个限制，我们可以将 fragment 组件作为根元素的占位节点，而不去渲染它。

## 快速应用
### 一、安装依赖

```bash
npm i vuejs-fragment -S
```

### 二、使用

- Plugin:

```vue
import Fragment from 'vue-fragment'
Vue.use(Fragment.Plugin)

// or

import { Plugin } from 'vue-fragment'
Vue.use(Plugin)

// …

export const MyComponent {
  template: '
  <fragment>
    <input type="text" v-model="message">
    <span>{{ message }}</span>
  </fragment>
  ',
  data() { return { message: 'hello world }}
}
```

- Component:

```vue
import { Fragment } from 'vue-fragment'

export const MyComponent {
  components: { Fragment },
  template: '
  <fragment>
    <input type="text" v-model="message">
    <span>{{ message }}</span>
  </fragment>
  ',
  data() { return { message: 'hello world }}
}
```
