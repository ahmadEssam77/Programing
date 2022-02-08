# Vue JS

##### There are four ways to install/use vue
1. CDN  (Content Delivery Network)
2. Download the JS file
3. Install it using npm
4. Use the official CLI  (Command Line Interface)

##### Vue devTools extensions allowing you to inspect and debug your Vue applications 

##### Single File Components (SFC)
```
Vue also provides accompanying tools for authoring SFC
```
**CLI** apply hot reload consipt, which is you can make changes to the code and apply them to the running application.

> **[Migration guide](https://v3.vuejs.org/guide/migration/introduction.html#overview) what's new in vue 3 if you know vue 2**

`element.mount("dom element");`

`v-bind:attribute="variable"`
`v-on:click="function"`
`v-model="variable"`  => two ways data binding

`v-if="variable"` => structure directive binding
`v-for="variable in arr"` => structure directive binding

> props to send data from child to parent

##### What is the custom element? (JS MDN)

```
> const app = Vue.createApp(rootComponent);
> app.mount("#html-element");
```
