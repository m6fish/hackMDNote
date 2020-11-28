那些尚未玩過的技術 Vue
===


[![hackmd-github-sync-badge](https://hackmd.io/uVKHYi5dR7mKd7J-OtOWAQ/badge)](https://hackmd.io/uVKHYi5dR7mKd7J-OtOWAQ)

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

### v-slot / slot name

[Named-Slots](https://vuejs.org/v2/guide/components-slots.html#Named-Slots)

> After 2.6.0, it replaces the **slot** and **slot-scope** attributes.<br/>
> ShortHand: replace v-slot: with #

```
v-slot:default={id, handleClick} 
#default={id, handleClick}

<slot v-bind={id, handleClick}/>
```


### Render Props

[render-function](https://vuejs.org/v2/guide/render-function.html)

> In some case when needing the full programmatic power of JavaScript.<br/>
> with JSX


### Passing Props & Listeners

[Transparent Wrapper Components in Vue](https://zendev.com/2018/05/31/transparent-wrapper-components-in-vue.html)

> Passing props and listeners to a child component without having to declare all.<br/>
> **inheritAttrs: false** (otherwise both, div and child-component will receive the attributes)


### Higher Order Component (HOC)

[Higher Order Components in Vue.js](https://medium.com/bethink-pl/higher-order-components-in-vue-js-a79951ac9176) <br/>
[vue-hoc simple](https://github.com/bognix/vue-hoc) <br/>
[Do we need Higher Order Components in Vue.js?](https://medium.com/bethink-pl/do-we-need-higher-order-components-in-vue-js-87c0aa608f48)

> HOC is a function that takes a component as an argument and returns a new component

> 類似於工廠模式

### Provider / Consumer

>  Separating stateful logic from the presentation.

> 透過父層，讓兄弟姊妹層可以互相呼叫

### Provide / Inject

[provide / inject](https://vuejs.org/v2/api/#provide-inject)

>  to provide object into **all its descendants** (in the same parent chain)<br/>
>  provide and inject bindings are **not reactive**

> 讓子孫層可以拿到祖先層資料的初值

### errorCaptured Hook

[errorCaptured](https://vuejs.org/v2/api/#errorCaptured)

[Handling Errors in Vue with Error Boundaries](https://medium.com/@dillonchanis/handling-errors-in-vue-with-error-boundaries-91f6ead0093b)

>Have you ever had a v-for not render the elements in your list due to an unforeseen error on only a single one of those elements?

> 確保元件不會因為單個資料壞掉，導致整個UI死掉

### Productivity Tips - watch on create

```
// don't
created() {
  this.fetchUserList();
},
watch: {
  searchText: 'fetchUserList',
}
```
```
// do
watch: {
  searchText: {
    handler: 'fetchUserList',
    immediate: true,
  }
}
```
**immediate: true**
> 讓監聽值在 **初始** 和 **值變動**時觸發 handler
