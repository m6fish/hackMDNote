那些尚未玩過的技術 Vue
===

###### tags: `技術` `Vue`

紀錄自己未使用過的Vue 2.x部分

## 資源


* [vue-patterns(英文原版)](https://github.com/learn-vuejs/vue-patterns)
* [Vue 實作模式 (vue-patterns) 中文版](https://github.com/yoyoys/vue-patterns-cht)

---

### Functional Component

>  no script tag, only "**props**"

* Faster rendering
* Lighter memory usage

### Renderless Component

>  not render any HTML, for Slots API

 * seperate logic from markup

### v-slot

[Named-Slots](https://vuejs.org/v2/guide/components-slots.html#Named-Slots)

> After 2.6.0, it replaces the **slot** and **slot-scope** attributes.<br/>
> ShortHand: replace v-slot: with #


### Render Props

[render-function](https://vuejs.org/v2/guide/render-function.html)

> In some case when needing the full programmatic power of JavaScript.<br/>
> with JSX


### Passing Props & Listeners

[Transparent Wrapper Components in Vue](https://zendev.com/2018/05/31/transparent-wrapper-components-in-vue.html)

> Passing props and listeners to a child component without having to declare all.<br/>
> **inheritAttrs** :false (otherwise both, div and child-component will receive the attributes)


## Higher Order Component (HOC)

[Higher Order Components in Vue.js](https://medium.com/bethink-pl/higher-order-components-in-vue-js-a79951ac9176) <br/>
[vue-hoc simple](https://github.com/bognix/vue-hoc) <br/>
[Do we need Higher Order Components in Vue.js?](https://medium.com/bethink-pl/do-we-need-higher-order-components-in-vue-js-87c0aa608f48)

> HOC is a function that takes a component as an argument and returns a new component


### Provide / Inject

[provide / inject](https://vuejs.org/v2/api/#provide-inject)


