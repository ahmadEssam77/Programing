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

##### Lifecycle Hooks Vue
```
Each component instance goes through a series of initialization steps when it's created - for example, it needs to set up data observation, compile the template, mount the instance to the DOM, and update the DOM when data changes. Along the way, it also runs functions called lifecycle hooks, giving users the opportunity to add their own code at specific stages.

> don't use arrow function with these methods, should write them created() {} or mounted() {} updated() {} unmounted() {} and so on
>in created() {console.log(this.counter)}  `this` refers to or points to the vm instance. ViewModel
```

##### Interpolation
#### Text
```
{{ message }}  Mustache syntax
v-once will change it one time only <span v-once> the message is {{ message }}</span>
but keep in mind this will also affect any other bindings on the same node
```
#### Raw HTML
```
data() {
  return {
    rawHTML: `<span style="color: red">Test</span>`
  }
}

<div id="app">
  <span v-html="rawHTML"></span>
</div>
```
#### Attributes
```
<button v-bind:disabled="Booleanvariable"></button>
```
#### Using JS Expression
```
{{ ok ? "yes" : "no" }}
{{ message.split('').reverse().join('') }}
```

##### Directives
Directives are special attributes with the v- prefix. Directive attribute values are expected to be a single JavaScript expression (with the exception of v-for and v-on, which will be discussed later). A directive's job is to reactively apply side effects to the DOM when the value of its expression changes.

##### arguments vs dynamic arguments
```
<a v-bind:href="url"></a>  (there are some constraints)

<a v-bind:[attributeName]="url"></a>
```

##### data() {}   function
##### methods: {}  option

# reactivity system

##### computed property and watchers  (data changes)
```
computed also vs methods
computed => It's a cached base on their reactive dependencies (means happens if there is a change)
method => is just a function bound to the Vue instance. It will only be evaluated when you explicitly call it.

watch => works with API and asynchronous
```
##### > Class and style binding
```
- it depends on truthness value
- can be object or array
```

##### Conditional Rendering
```
v-if || v-else-if || v-else
v-show
The difference is that an element with v-show will always be rendered and remain in the DOM;
v-show doesn't support the <template> element, nor does it work with v-else.
v-show if you need to toggle something very often, and prefer v-if if the condition is unlikely to change at runtime.
```

##### list rendering
```
v-for directive
for reversing matter while dealing with arrays or do some operations, the best approache to make it in computed: { return ..}
also you have to make a clone or a copy from the original array so we use spread operator return [...numbersArray].reverse() instead of numbersArray.reverse()
```

##### Event handler
```
- inline handlers and methods handlers
- event modifiers
```
##### Form input binding
```
v-model with almost all input types
```

### Top 10
```
- Computed property (done)
- Event handling || listen for an event.
- Lazy loading || Async components
- Global components
- Single file component
- Testing
- CLI Tool   (vue serve component path)  (vue build --target lib --name goldenRule component path) to share a specific component with someone
- Props management
- Server-side Rendering (SSR)
- Deployment
```
