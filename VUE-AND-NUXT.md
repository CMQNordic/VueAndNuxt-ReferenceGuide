## ___VUE.JS  &  NUXT___

---

By&nbsp;Martin&nbsp;Czerwinski [CMQ&nbsp;Nordic.](www.cmq.se)
&nbsp;March&nbsp;2020.

---
This is a compact tutorial & reference document for vue.js and nuxt.<br>
_Vue.js_ is a modern open source java script framework for
building modern front-end user interfaces and single-page applications.<br>
_Nuxt_ is ... TODO

Share this page, bookmark it and feel free to
[__reach out to us__](www.cmq.se 'Contact us!') with questions, comments or requests for assignments!

---

#### __TABLE OF CONTENT__

- [__1. Vue.js__](#vue-js)
  - [Vue vs React vs Angular](#vue-vs-react-vs-angular) ◦ [Get started wih Vue](#get-started-with-vue) ◦ [Structure of your project](#structure-of-vue-project)
  - [Basics of Vue](#basic-of-vue)
  - [Custom events](#components-communication-in-vue)
  - [Single-file components](#single-file-components-in-vue)
  - [Slots & Components](#slots-and-components-in-vue)
  - [Directives](#directives-in-vue)
  - [XXX](#basics-of-m) ◦ [XXX](#import-data-into-a-query-in-m) ◦
    [XXX](#types-values-in-m)

- [__2. Nuxt__](#nuxt)
  - [__Get started__](#get-started-with-nuxt) ◦ [Structure of Nuxt projects](#structure-of-nuxt-projects)
  - [Basics of Nuxt](#basics-in-nuxt)
  - [Routes](#routes-in-nuxt) ◦ [XXX](#import-data-into-a-query-in-m)

<br>

## __[1. Vue.js]()__


<br><p align=right><a id="get-started-with-vue" href="#table-of-content">↩ Back To
Top</a></p>

### [__Vue vs React vs Angular__]()

---

Vue alternatives - React and Angular - are other popular javascript frameworks. 

React was released in 2013 by Facebook and is mostly used in high traffic websites. Is is more like a library as it has less default build in features (for example routing witch vue offers is out of the box). It depends a lot on comunity packages.  Whatsapp, Instagram Paypal, BBC are some of the popular companies use react.

Angular was released in 2010 by Google. It is a typescript based javascript framework. It is heavy and have more default build in features than vue. It is specially popular in enterprice world among big companies. Google and Wix are among the most popular companies using Angular.

Vue is a progressive Javascript framework (base included and add-ons like plugins can be installed), released in 2014 and developed by no big name like React and Angular. It is the youngest member of todays most popular Javascript frameworks. It has practically removed the drawbacks of the other frameworks to offer ease of software development. It supports typescript from version 3. Websites like GitLab and Alibaba are using Vue. At the moment vue is very populat for fast prototyping. Its a bit less popular among big companies. Yet it is growing in popularity fast.

Important to know is something called DOM, which can be understood as UI (that is the user interface) of your application. The DOM changes whenever you update the UI, this represents the changes that are made in the application. It can be used in two ways, either as virtual DOM or a real DOM. The performance of the framework/library is highly affected by how DOM is handled.

Angular uses real DOM. It is extremely hard to handle because if you lose the flow, you will have to go deep into the code to
actually find out the issue. It also might results in bit slower ui performance.

React uses virtual DOM. It is very lightweight. It is provided in react package for free and eliminates the issues of slow performance of real DOM. Significant improvement in the performance of javascript frameworks/ libraries and made React utterly popular.

Vue uses virtual DOM too. This ensures faster ui performance. Vue is the lightest of all those above. Vue and React offers better performance and flexibility than Angular. Vue and React are more suited for light-weight applications and angular is the best for large UI applications. Angular is highly opinionated and unlike Vue and React, it offers everything from routing, templates to testing utilities in its package (that is of course more heavy). Vue and React do not require to hire web developers who are proficient in typescript. But among these two Vue has an upper hand as it is considered more friendly by the developers. Angular is actualy diminishing in popularity as in 2020.

<br><p align=right><a id="get-started-with-vue" href="#table-of-content">↩ Back To
Top</a></p>

### [__Get started with Vue__]()

---

Vue team provided an official CLI (Command Line Interface) called "vue CLI". It´s main task is to quickly scaffold (autogenerate) configured templated projects for us. Is helps us to select libraries and functionality our project will use and if needed configures webpack to get properly bundled together and optimized for development. It not only provides command line shortcuts but also a handy graphical interface to setup or change our project. As a result you can get started very rapidly and easily with just a few clicks. Important to note is that version 3.0 of "vue CLI" is NOT version 3.0 of Vue (but actually Vue 2.0). "Vue" and "Vue CLI" are separate codes and separate version's! Vue CLI is similar to _Angular CLI_. Among other things it hides the complexity of having to know how webpack or babel work. It's also pluggable, meaning you decide when you start to use TypeScript, Babel, Unit Testing and later add on functionality. It also allows you to run builds, watch for build changes or even just serve an HTML file to development. Vue CLI is the right way to get started with a vue project but it is  assumed prior knowledge of Node.js and the associated build tools! CLI set up of project usually create a project with many folders and Webpack specific files and settings therfore be users that use Vue CLI shall know what the chosen component of the project are.

 To check your current vue-cli version run in command window __`vue --version`__.

Detailed Vue installation guide ---->
[VUE INSTALLATION](https://vuejs.org/v2/guide/installation.html#CLI)

#### Install and gest started with Vue

1. Install nmp <br>To start you must have _nmp_ installed globally to provide executable command that you run from the shell and to be reused across projects. Some packages are just better installed globally and npm, gatsby-cli or vue-cli are some of them.

2. Install vue-cli:<br>

    > __`npm install -g @vue/cli`__ -> installs vue-cli globally<br>

    After installation you will have access to the _vue binary_ in your command line. Run __`vue`__ command in shell to double check if the installation was ok.

    Note!<br> Up to vue-cli v.2 we used `vue init [template]` command, with chosen project templates (i.e. webpack, webpack-simple, browserify, simple etc). In vue-cli v.3 forward
    this has been changed and the projects are now initiated by __`vue create`__ command following a wizard. Additionally from v.3 a GUI can be used to create projects and it is started with by command __`vue ui`__.

3. Create new vue project

    You can create a project in 2 diffrent ways.

    > __`vue ui`__ -> start new project from GUI<br> or<br> >
    > __`vue create <your-project-name>`__ -> follow command wizard with configuration options

    _If you of any reason still need the legacy `vue init` functionality, you can install a global bridge. A light template recommended for for simple prototyping is named `webpack-simple`_ <br>

    _`npm install -g @vue/cli-init`<br>
    `vue init webpack-simple <your-project-name>`_

4. Start created project
    > Navigate into the project folder in command line and write the command __`npm run serve `__ -> this will build the project and serve it at our local host<br> 

Note!<br> Avoid &-characters in folder names in you projects. If absolute path to <you-project-name> contains &-characters you might experience strange errors when in background running webpack-dev-server!


<br><p align=right><a id="structure-of-vue-project" href="#table-of-content">↩ Back To
Top</a></p>

### [__Structure of your project__]()
---
[CSS](#css-vue) ◦ [BEM](#bem-vue) 

Generally it is recommended to give your project a structure that is easily maintenable in the future and easy to understand by others (or you self looking at it month later on). This chater is not Vue specific.

__<a id="css-vue">CSS</a>__

To start with, read the blog from an authority in the web design industry Nicolas Gallagher on the topic of class names - [here](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/).  

> The most reusable components are those with class names that are independent of the content. We shouldn’t be afraid to include additional HTML elements if they help create more robust, flexible, and reusable components. Doing so does not make the HTML “unsemantic”, it just means that you use elements beyond the bare minimum needed to markup the content.  
> 
> The primary purpose of a class name is to be a hook for javascript and css. 
>  
> Class names should communicate usefull information to developers.


In larger projects there might be a need to have global styles applied to whole application and consistent styling to some common elements. Beyond the scoped attribute, using unique class names can help ensure that 3rd-party CSS does not apply to your own HTML. For example, many projects use the button, btn, or icon class names. To ensure we recommend to prefix the class name in a way to ensure uniqueness. We recommend word `app` or your company initials like `cmq`.
```h
- assets
  - styles
      - global
        XXX
          - _colors.css // colors used within the app here
          - _variables.css // variables independent of environment prod/dev
          - _mixins.css // postcss mixins like @media
        global.css // to be marked as global CSS in nuxt.config.js

      - modules
          - _app-link.css // add app prefix to ensure uniqueness 
          - _app-button. // _ means "partial file" -> to be imported in other files
  -

```  

__<a id="bem-vue">BEM</a>__

With BEM (Block-Element-Modifier methodology) you can create a modular, consistent and reusable structure for your style-sheets which is easier to understand & use.

_Block _ 
Styles are broken up into blocks, which is typically a container that wraps many elements. For example, a footer would be a block.  
```
.footer {}  
```
_Element_  
Many elements make up a block. Usually elements do not have any semantic meaning outside of the block.
```
.footer__logo {}
.footer__social {}
.footer__text {}
```
_Modifier_  
A modifier is focused on changing how the element looks visually and/or controls its behavior.
```
.footer__text--bold { }
.footer__text--green { }
```

<br>

> In scoped styles the BEM naming scheme might not seem to be necessary anymore. But  still a lot can be gained as having an indicator when to split up your components into multiple smaller ones. Advantages of BEM-ifying class names even if scoped are: __1)__ Gives you an __indicator when the component could be split__ in smaller ones when you stating to get out-of class-names. Read more [here](https://markus.oberlehner.net/blog/how-the-bem-css-naming-scheme-can-improve-vue-component-architecture/).

> Scoped styles are pretty nice, but can have some potential pitfalls if working with a larger team. Advantages of BEM-ifying class names even if scoped are:__ 1)__ helps __prevent any conflict with another component__ for cases our team forgot to add `scoped` to the style tag. __2)__ __Testing/QA automation__ to have enough specificity on class names to distinguish elements. Read more [here](https://spectrum.chat/vue-js/help/bem-and-scoped-styles~f573992a-7ca4-414c-896e-17b37eb18da7?m=MTUyMjgxNTg5OTI5MQ==).

> BEM makes it __easier to implement multiple visual appearances__ (themes), also personally we feel very comfortable to support styling using BEM because it is easy to follow different visual styles of component. Read more [here](https://medium.com/@imanhodjaev/bem-styled-components-case-with-vue-d15901bf762e). 

> BEM structure together with nesting can give you reusable components easy to copy where only the main class name need to be changed as the element & modifier with general namin can be reused. 


Nesting CSS
Descendant selectors goes against BEM philosophy and often create [specificity wars](https://stuffandnonsense.co.uk/archives/css_specificity_wars.html) that can result in unexpected behavior. As the CSS Specificity is one of the most difficult concepts to grasp in Cascading Stylesheets, appliing BEm solves most of the trouble.
```h
BAD - descendant selector

.header {
  .button {
    .green {
      color: green;
    }
  }
}

// Results in a "descendant selector" -> specificity wars -> risk for errors

.header .button .green {
  color:green;
}
```
```javascript
GOOD - direct selector

.header {
  $__button {
    &--green {
      color: green;
    }
  }
}

// Results in a "direct class selector" -> less errors

.header__button--green {
  color:green;
}
```


<br><p align=right><a id="basic-of-vue" href="#table-of-content">↩ Back To
Top</a></p>

### [__Basics of Vue.js__]()


---

[Basic example](#basic-example-of-vue) ◦ [Instances](#vue-instance-vue) ◦ [Attributes](#attributes-vue) ◦ 
[Components](#components-vue) ◦ [Computed vs Method](#computed-vs-method-vue) ◦
[Event modifiers](#event-modifies-vue) ◦ [Key modifiers](#key-modifies-vue) ◦
[Props](#props-vue) ◦ [Native properties in this](#native-properties-in-vue) ◦
[Classes and Styles](#classes-and-style-in-vue) ◦
[Life-hooks](#life-hooks-in-vue)

First some general facts about vue that are important to know and understand!

ECMAScript is the official name of JavaScript. Version ECMAScript 7 is also known as ES7, ECMAScript 2016 or JavaScript 7. Not all browsers may support ES7 syntax but we still can use the latest version of javascript in our projects as webpack (or babel) transforms (when building our app) latest ECMA code into valid javascript syntax that all browser supports.

Some Vue syntax & functionality changed with recent Vue version 3 (late 2020). For example creating and connecting vue to a tamplate changed a bit. in examples below we demonstrate version 2 and the newest version 3 setup. Also for examples to work in projects without preprocessors (like Webpack) we in basic examples use pure ES5 syntax in order to work on all browsers.

Generally Vue under the hood "encapsulates" commonly used javascript functionality for us. Simply explained it provides us a special syntax how to define the final result we want the javascript to perform. Vue creates all necessary javascript for us, in the background.

A part of HTML must be defined and labled to be reached by vue to render it. For that Vue uses HTML-based template syntax that is in background rendered and bound to virtual DOM. Vue can intelligently figure out the minimal number of components to re-render and apply the minimal amount of DOM manipulations when the app state (something in UI) changes. 

We can use vue in 2 diffrent ways in order to apply Vue code to our HTML code. We can target vue to only parts of our HTML pages (kind of "vue-widgets" within existing HTML i.e only a chat functionality written in vue), or to whole HTML page that is controlled by vue (more common, single page application). Both approaches in genarel have same vue structure but are integrated in our site a bit differently. Also referencing to HTML templates differs for those 2 approaches.

Vue.js API can be found --> [here](https://vuejs.org/v2/api/). 

Learn basics about Vue --> [here](https://vuejs.org/v2/guide/syntax.html).  


__<a id="basic-example-of-vue">Basic example</a>__  

![Vue instance lifecycle](assets\images\basic_example_v2.jpg)

Following example can be reached on jsfiddle.com<br>
 [Basic Example Vue V.2](https://jsfiddle.net/martin_cmq_nordic/ch64syad/)


```html
<!-- Import vue v.2 package -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>

<section><b>Basic Vue Example</b></section><br>

<!-- only this section is controlled by vue -->
<div id="app">
	Name:<input v-model="name">
	<button @click="age++">Increase age</button>
	<p>
      Name is: <span class="empty">{{ getName() }}</span> 
      Age is: <span class="empty">{{ currentAge }}</span>
  </p>
</div>

<script>
var app = new Vue({
	el: '#app',
	data: {
		name: '',
		age: null,
	},
	methods: {
		getName: function() { return this.name }
	},
	computed: {
		currentAge: function() { return this.age }
	}
})
</script>

<style>
	.empty {
		display: inline-block;
		height: 16px;
		min-width: 40px;
		background-color: lightgrey;
		border: 1px dotted black;
	}
</style>
```

Following example can be reached on jsfiddle.com<br>
 [Basic Vue Example V.3](https://jsfiddle.net/martin_cmq_nordic/ch64syad/)

```html
<!-- Import vue v.3 package -->
<script src="https://unpkg.com/vue@next"></script>

<section><b>Basic Vue Example</b></section><br>

<!-- only this section is controlled by vue -->
<div id="app">
	Name:<input v-model="name">
	<button @click="age++">Increase age</button>
	<p>
      Name is: <span class="empty">{{ getName() }}</span> 
      Age is: <span class="empty">{{ currentAge }}</span>
  </p>
</div>

<script>
  <!-- Create new vue instance  -->
  var app = Vue.createApp({
    data: function() {
      return {
        name: '',
        age: null
      }
    },
    methods: {
      getName: function () { return this.name }
    },
    computed: {
      currentAge: function () { return this.age }
    }
  })

<!-- Connect the instance with a template -->
app.mount('#app')
</script>

<style>
	.empty {
		display: inline-block;
		height: 16px;
		min-width: 40px;
		background-color: lightgrey;
		border: 1px dotted black;
	}
</style>
```
_Note! As see in version 3 we use function createApp on vue object and data is a function. Those are the main changes in version 3._


|||
|---|---|
|math.random|random between 0 na d 1|
|||


__<a id="vue-instance-vue">Instances</a>__<br> 
A Vue instance is essentially a ViewModel as defined in the MVVM pattern, hence the variable name vm you will see throughout the docs. When you instantiate a Vue instance, you need to pass in an options object which can contain options for data, template, element to mount on, methods, lifecycle callbacks and more.

_Vue Ver 2_: Create instance by `const vm = new Vue({...})` (vm stands for Vue Model). <br>
_Vue Ver 3_: Create instance by `const vm = Vue.createApp({...})` (vm stands for Vue Model).

Note that in version 3 we must connect the instance with a templeta by `mount('#[id]')` command. After that interpolation works (accessing data from javascript). This means that syntax in HTML that is controlles by vue like `{{ [parameter_mane_in_javascript] }}` is behind the scenes changed to pure HTML  by View - parameters from javascript (vue code) are then directly accessed from HTML. This is one of the main features of reactivness in vue.

When creating an Vue instance we must provide attributes like `data` or `methods` etc as input. We can later access those attributes by calling `vm.<attribute>`or `this.<attribute>` within the instance or component. We can also access the `vm` object from other instances or normal java script functions.  

Main vue app instance is usually created in `main.js` file.

__<a id="vue-directives">Build in directives</a>__<br> 

The interpolation {{}} or v-bind attribute you see in vue controlled HTML code are called a directives. Directives are prefixed with v- to indicate that they are special attributes executed by Vue and they apply special reactive behavior to the HTMl (though vue & virtual DOM). There are some build in directives that work out of the box in vue. There is also possibility to create self defined directives.

More about:<br>
DOM event objects ---> [HERE](https://www.w3schools.com/jsref/dom_obj_event.asp)<br>
Event handling in Vue.js ---> [HERE](https://vuejs.org/v2/guide/events) <br> 
Event modifiers in Vue.js ---> [HERE](https://vuejs.org/v2/guide/events.html#Event-Modifiers)

||||
|---|---|---|
|`{{ [data] }}`|Text interpolation. Adds data property as text in HTML. HTML in data interpreted as text as protection for cross side script attacts.|`<p>My name is {{name}}</p>`|
|`v-html="[data]"`|Adds data property as HTML between HTML tags.|`<p v-html="data"`></p>|
|`v-bind:[attribute]=[data]`<br> or <br>`:[attribute]=[data]`|One way binding. Binds vue data property to HTML attribute.| `<img v-bind:src="image">` or `<img :src="img-link">`|
| `v-model="[data]"` |Two way binding. Binds vue data property to HTML field and at same time if changed in vue then back to HTML.| `<input v-model:"name"><p>{{ name }}</p>`|
| `v-on:<event>`<br>or<br> `@<event>`                              | Sends own param and/or event from HTML template to Data                                                                                                                                    | `<button v-on:keydown ="keyDown(2, $event)">Click me<button>` or short `<button @keydown ="keyDown(2, $event)">Click me<button>` |
| `@<event>.stop`                                                  | Stops the bubbling of an event to parent elements, `stopPropagation()`. Use prevent for `preventDefault()`. Event modifiers [here](https://vuejs.org/v2/guide/events.html#Event-Modifiers) | `<button @click.stop">Click me<button>`                                                                                          |
| `@<key-event>.enter.space`                                       | Trigger event function only for `enter` & `space` keys. Event modifiers [here](https://vuejs.org/v2/guide/events.html#Event-Modifiers)                                                     | `<input @keyup.enter.space ="func">`                                                                                             |
| `v-if:"true/false"`                                              | Binding visibility of element to Data property                                                                                                                                             | `<span v-if:"bVisible">Visible or not</span>`                                                                                    |
| `v-for="i in <array>"`                                           | Display list of items based on Array in Data                                                                                                                                               | `<ol><li v-for="i in arrayX">{{ i.text }}</li></ol>`                                                                             |


<br><p align=right><a id="examples-of-vue" href="#table-of-content">↩ Back To
Top</a></p>




__<a id="attributes-vue">Attributes</a>__

_ES6/7 syntax is applied as babel and webpack transforms it to valid browser syntax when building the app_



__`▸ el`__  
 Reference name of HTML element (id -> #app) to apply the Vue instance on. (only ver 2)
```javascript
el: 'app'
```
 __`▸ data`__  
 Declaration of properties of non-reactive variables to
 use within an instance. No calculations possible here. Can be reached from
 `this`. Note! If used in a component or vue ver 3, then this must be a returning function.

 ```javascript
data() {
  return {
    name: 'Martin'
  }
}
```
 
 __`▸ props`__  
 Data passed to a child component from parent. To be used in same manner as data properties. Can be re-rendered (reset) by parent though.  
```javascript
props: {
  name: {
    type: String,
    default: 'Martin'
  }
}
```
 __`▸ computed`__  
 Functions that are executed(recalculated) ONLY when variables they are bound to are changed. When binding changing variables is better to use computed functions (instead of binding to methods or data) as they are executed only when the values is bids to change.
```javascript
computed: {
  name() {
    return this.name 
  }
}
```
__`▸ methods`__  
 Functions that can be called for execution. Note! When binding to a method then is might be executed unnecessarily even if variables that is used in method did not change state. Often used to handle events and emit events.
```javascript
methods: {
  getName() {
    return this.name
  }
}
``` 
__`▸ watch`__  
Listener for changes in properties. Set of functions/callbacks to be executed only if corresponding property change.  
```
watch: {
  name: function (val, oldVal) {
    console.log('Name changed: New: %s, old: %s', val, oldVal)
  }
}

```
 __`▸ created/mounted/updated`__  
 Life-cycle hooks. Functions to execute it diffrent "states" of an instance or component.
```javascript
created () {
  // called when ... 
  ...
},
mounted () {
  // called when ... 
  ...
},
updated () {
  // called when ... 
  ...
}
``` 
 __`validation`__ - Function called before component is loaded. Only when returns true then loaded.  


__<a id="components-in-vue">Components</a>__<br> Vue components are extensions
of vue instances. Given a name it can be reused in instances and other components.
This (together with instance) is the main building block of Vue applications.

There are several ways to create a component. Usually parameters like `data`,
`methods`, `computed` and `props` are defined on the component itself and valid
locally within this component only. 


A template can be an textual attribute like `'<p>Hello world</p>'`, a reference
to HTML element id but the far most useful (and powerful) method of defining
templates is to use template definition in _single-file components_ (separate
.vue files). For this to work a _vue-loader_ plugin must be executes by a
bundler like Webpack, therefore for this to work our files must be
compiled/bundled with webpack and vue-loader to be executable in a browser.
Generation vue project with ue of vue-cli fix this setup for you in such case.

Naming of a component is important and can be as _kebab-case_
`my-component-name` or _PascalCase_ and actually both at same time. When
defining a component with _pascalcase_ like `MyComponentName` is can be reached
in HTML as `my-computed-name` also.

```javascript
<script>
// If developing with bundlers like Babel & Webpack
// templated single-file component can be imported
// from a separate .vue file.
import componentY from './ComponentY.vue'

// Component can also be defined as an js-object
var componentX = { data: function()  }

// Global definition of component
Vue.component('my-component-x', componentX )

// Local definition of components
new Vue({
  el: '#app',
  components: {
    'my-component-x': componentX,
    'MyComponentY': componentY
  }
})
</script>
```

__<a id="single-file-components-in-vue">Single-file Components.</a>__<br> When
creating a component in traditional way with dedicated Vue.component() function
or in

__<a id="computed-vs-method-vue">Computed vs Method.</a>__<br> In example above
when "Increase Counter" is pressed both `getCounterByComputed` and
`getCounterByMethod` functions are executed - as expected. But when "Increase
Dummy" is pressed only `getCounterByMethod` is executed. This because Vue checks
if a computed function has dependency to any data property that changed before
running the function. Here not, as dummy is not used in `getCounterByMethod`
function, therefore no need to run this function. Performance saver!

__<a id="event-modifies-vue">Event modifiers.</a>__<br> Event can be modified to
do different things when cached. Here for example do `event.stopPropagation()`
by simply adding `stop` after event as below. Read about more types of modifiers
[here](https://vuejs.org/v2/guide/events.html#Event-Modifiers). <br>
`<span @mousemove.stop=""></span>`

__<a id="key-modifies-vue">Key modifiers.</a>__<br> For key-events we can bind
certain keys to react for. Here for example execute alert function only when
`enter key` was pressed.<br><br> `<input @keyup.enter="alert('enter pressed')">`

__<a id="props-vue">Props.</a>__<br> Props are properties set from outside and
passed into the component. Props can be of primitive or reference type. Props in
component be set as simple array of names, or with validation. Validation of
props is good to use as we get warnings in console at dev time when we send to a
component something a datatype we do not expect.

When sending _primitive types_ like String or Number into a component the memory
is copied and changes to property inside the component are not visible outside.
But note that when mutating such a prop the value in the component will be
overwritten whenever the parent component re-renders.

When sending _reference types_ like Function, Array or Object as a prop to a
component then only the pointer to the memory is sent and the component do not
"owe" the property. The changes to this property (or function call) within the
component will be visible outside.Example:

```javascript
props: [['propName1', 'propName2', 'propName3']
OR
props: {
	// => Use as a normal property
	// short
	propName1: String,
	// with validation default: can be set if not required
	propName2: {
		type: Number,
		required: true
	},
	// object validation
	propName2: function() {
		id:  Number,
		name: String
	}
}
```

__<a id="native-properties-in-vue">Native properties in _`this`_.</a>__<br>
Properties in __`this`__ (Vue instance struct) starting with `$` are the native
vue objects we can access.<br>

__`$el`__: el object in constructor to be reached through this<br>

__`$data`__: the data object in constructor to reach properties with
`this.$data.<property-name>`

__`$refs`__: The `ref` that we can set on any HTML element to refer to it
easily. Note that using this is not recommended for setting DOM elements as Vue
template when rendered will overwrite those. It is good to use
`this.$refs.<ref>` for accessing native elements in DOM.

Example:

```html
HTML
<button ref="myButton"></button>

SCRIPT this.$refs.myButton.InnerText="Press Me" // Note! to reach a ref an
instance the life-hook mounted() to DOM shall be executed in order for all refs
to be set.
```

__<a id="classes-and-style-in-vue">Classes and Styles.</a>__<br> There are two
ways to bind the class or css style to an HTML object. Vue will concatenate the
classes - those defined normally by class with those through bound with are
v-bind.

```html
// Class bound as an array of class names
<div class="some-class" :class=['className1', 'className2']></div>

// Class bound as key/value objects where key is either true/false deciding if this class shall be enabled or not.
<div class="some-class" :class={'class-Name1': true, className2: false}></div>
```

__<a id="life-hooks-in-vue">Life-hooks.</a>__<br> Read more here about
understanding
[Vue.js Lifecycle Hooks](https://www.digitalocean.com/community/tutorials/vuejs-component-lifecycle)
![Vue instance lifecycle](assets\images\instance_lifecycly.jpg)

Instance life cycle can be reached by:<br>

```javascript
mounted: function() {
	this.$refs.myButton.innerText = 'Set age to 23 in app1';
},
```

<br><p align=right><a id="components-communication-in-vue" href="#table-of-content">↩
Back To Top</a></p>

### [__Custom events__]()

---

[Parent->Child](#parent-child-communication) ◦
[Child->Parent](#child-parent-communication) ◦
[Component<->Component](#component-component-communication)

__<a id="parent-child-communication">Props</a>__ - parent -> child<br>

```html
When sending String or Number into a component the memory is copied and changes
to property inside the component are not visible outside. But note that when
mutating such a prop the value in the component will be overwritten whenever the
parent component re-renders. When sending Function, Array or Object as a prop to
a component then only the pointer to the memory is sent and the component do not
"owe" the property. The changes to this property (or function call) within the
component will be visible outside.

 _____________PARENT_________________
<!-- Sending probs down to child -->
<child-component :id="2" :name="'Martin'"></child-component>

<script>
  import ChildComponent from './ChildComponent.vue';

  export default {
    components: {
      ChildComponent
    }
  }
</script>

_____________CHILD______________
<!-- Child receives the probs -->
<script>
  export default {
    props: {
      id: {
        type: Number,
        required: true,
      },
      name: {
        type: String,
        default: 'name not defined',
      },
    },
  };
</script>
```

__<a id="child-parent-communication">$emit</a>__ - child -> parent 

```html
Child component can emit (trig) an custom event upward to parent with event
data. This method can not be used to send data to other child components. Must
then go though parent. 

_____________PARENT_________________
<!-- Parent listens to emitted event and reads $event data -->
<template>
  <p>{{ name }}</p>
  <child-component @eventFromChild="name=$event.name"></child-component>
</template>

_____________CHILD______________
<!-- Child send event (emit an event) up to parent -->
<script>
  methods: {
  	onClick() {
  		this.$emit('eventFromChild', {
  			id: 2,
  			name: 'Anna'
  		})
  	}
  }
</script>


```

__<a id="component-component-communication">Component <-> Component</a>__ (emit
on `eventBus` instance)

```html
_____________main.js____________
<!-- export new empty vue instance from script -->
export const appEventBus = new Vue(); _______Component Sender_________
<!-- component sending event on the bus -->
<script>
  import { eventBus } from "./main";

  methods: {
  	onClick() {
  		// emitting an event
  		eventBus.$emit('eventOnBus', {
  			id: 2,
  			name: 'Anna'
  		})
  	}
  }
</script>

_______Component Listener_______
<template>
  <p>{{ name }}</p>
</template>

<!-- component listening for event on the bus -->
<script>
  import { eventBus } from "./main";

  created() {
  	// when life-hook created reached, set up listener for the event
  	appEventBus.$on("logEvent", (person) => {
  		this.name = person.name;
  	});
  }
</script>
```

<br><p align=right><a id="single-file-components-in-vue" href="#table-of-content">↩
Back To Top</a></p>

### [__Single-file components__]()

---

__Components__ extend _Vue instances_ and are reusable in other components. We
can use components as a custom element. Components can be declared __globally__
or __locally__ in an instance. In more complex projects single-file components
(with a .vue extension) should be used together with build tools such as Webpack
or Browserify that auto-generate javascript that is served to browser.

When using vue-cli to start project a project template with auto-generated
configuration is set up for you. `Webpack.config.js` file defines tools and
bundles all our files to one build.js that is serves to the browser.
`Package.json` file define packages to use and scripts to run.

Simple project based on single-file template can look like this:<br> Here we
have a Parent instance defining 3 components and using those as children (2
`ClickCounter` components and 1 `Logs`). Parent send __`props`__ to children and
on eof those is a callback function that children directly can execute. Both
`ClickCounter` children __`emit`__ even up to parent telling about changes. All
components are sending log events on the __`eventBus`__ and Logs component is
listening to those and viewing the logs.

__This example__ demonstrates structure of an vue application using single-file
templates and communication between parent, children and between components.

![image](assets\images\click-counter.JPG)

__index.html__

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Basic single-file application</title>
  </head>
  <body>
    <!-- Our app defining vue and "app" -->
    <div id="app"></div>

    <!-- Webpack is configured by "webpack.config.js" file to builds and bundle
	all project files one script "build.js" that is placed in "dist" folder -->
    <script src="/dist/build.js"></script>
  </body>
</html>
```

__main.js__

```javascript
// "webpack.config.js" points out this file
// as starting point with "entry: './main.js'"
//
// Imports Vue framework, creates new "app" instance and
// an instance for communication with events.
// Render main single-file template App.vue
// that replaces element "app" in index.html file.

import Vue from 'vue';
import App from './App.vue';

export const appEventBus = new Vue();

new Vue({
  el: '#app',
  render: (h) => h(App),
});
```

__App.vue__ (component: Parent)

```html
<template>
  <div class="container">
    <h3>Parent</h3>
    <button @click="resetAll()">Reset all</button>{{ getAllCounters }}
    <!-- Sending (mutating) counters to children on purpose. Re-render in parent will reset values in children -->
    <!-- By sending callback function resetAll() children can execute in parent -->
    <!-- Children inform about counter changes through "counterChanged" event -->
    <app-click-counter
      :compName="'A'"
      :counter="counterA"
      :resetAllCB="resetAll"
      @counterChanged="counterA=$event"
    >
    </app-click-counter>
    <app-click-counter
      :compName="'B'"
      :counter="counterB"
      :resetAllCB="resetAll"
      @counterChanged="counterB=$event"
    >
    </app-click-counter>
    <app-logs></app-logs>
  </div>
</template>

<script>
  import ClickCounter from './Components/Temp/ClickCounter.vue';
  import Logs from './components/Temp/Logs.vue';

  // Parent need to send event on the bus (that log listens to)
  import {appEventBus} from './main';

  export default {
    // local components used from withing here
    components: {
      'app-click-counter': ClickCounter,
      'app-logs': Logs,
    },
    data: function () {
      return {
        counterA: 0,
        counterB: 0,
      };
    },
    computed: {
      getAllCounters() {
        return ' Counters: A=' + this.counterA + ' B=' + this.counterB;
      },
    },
    methods: {
      resetAll() {
        this.counterA = 0;
        this.counterB = 0;

        // Send event on the bus to those who listen
        appEventBus.$emit('logEvent', {
          source: 'Parent',
          text: 'resetAll() executed. All counters set to 0.',
        });
      },
    },
  };
</script>

<style>
  .container {
    background-color: grey;
    padding: 10px;
  }
</style>
```

__ClickCounter.vue__ (Components: A and B)

```html
<template>
  <div class="button-counter">
    <h3>Component: {{ compName }}</h3>
    <button @click="increaseCounter(1)">
      You clicked here {{ counter }} times
    </button>
    <button @click="increaseCounter(null)">Reset this</button>
    <!-- when clicked call a callback in the parent that resets all counters -->
    <button @click="resetAllCB()">Reset all</button>
    <p v-if="counter > 0">{{ "Counter: " + counter }}</p>
  </div>
</template>

<script>
  import {appEventBus} from '../../main';

  export default {
    props: {
      compName: {
        type: String,
        required: true,
      },
      // mutated prop, can be overwriten from parent
      counter: {
        type: Number,
        required: true,
      },
      // callback that resets the mutated counter
      resetAllCB: {
        type: Function,
        required: true,
      },
    },
    methods: {
      increaseCounter(value) {
        if (value == null) {
          this.counter = 0;
        } else {
          this.counter += value;
        }

        // emit an event up to parten informing about counter change
        this.$emit('counterChanged', this.counter);

        // Send log event on the bus to those who listen
        appEventBus.$emit('logEvent', {
          source: this.compName,
          text: 'Counter increased to ' + this.counter,
        });
      },
    },
  };
</script>

<style>
  .button-counter {
    background-color: beige;
    border: 1px solid black;
    margin: 10px 0;
    padding-left: 10px;
    padding-bottom: 10px;
  }
</style>
```

__Logs.vue__ (Component: Logs)

```html
<template>
  <div>
    <button @click="logs = []">Clear log</button>
    <div class="log">
      <h3>Component: {{ compName }}</h3>
      <p v-for="log in logs" :key="log.id">
        {{ log.source }}:
        <span class="log-message">{{ log.text }}</span>
      </p>
    </div>
  </div>
</template>

<script>
  import {appEventBus} from '../../main';

  export default {
    data: function () {
      return {
        compName: 'Logs',
        logs: [],
      };
    },
    // when created (life-hhok) set listener to log events
    created() {
      appEventBus.$on('logEvent', (log) => {
        this.logs.push(log);
      });
    },
  };
</script>

<style>
  .log {
    background-color: white;
    padding: 3px;
  }
</style>
```

<br><p align=right><a id="slots-and-components-in-vue" href="#table-of-content">↩
Back To Top</a></p>

### [__Slots & Dynamic Components__]()

---

Slots help you distribute code in other components. Good to build reusable
widgets like a slideshow. A template can contain a named slot that can be
dynamically modified from outside. Default content in single-file template slot
can be added and it is shown until the slot is not used/filled with content.

Note that parent is rendering both style and text before from outside the
template (style rendering from the child itself is possible too)

```html
CHILD - "my-template"
<template>
	<div>
		<h1 name="title">Title</ha1>
	</div>
	<div>
		<p class="my-subtitle" name="subtitle">Subtitle</p>
	</div>
</template>

PARENT -populating the slots
<my-template>
	<span slot="title">My Tilte</span>
	<span class=".my-content" slot="subtilte">{{ text }}</span>
</my-template>

<script>
export default {
    data() {
        return {
            text: 'My Subtitle'
        }
    },
};
</script>

<style scoped>
	.my-subtitle {
		color: darkcyan;
		font-size: larger;
	}
</style>
```

<br><p align=right><a id="directives-in-vue" href="#table-of-content">↩ Back To
Top</a></p>



### [__Examples__]()
---

Example: Adding a list:

Two componets. Items component holds logic and items in a list or array. Item is a single 

<my-items>
  <my-item></my-item>
</my-items>

<br>
<br>
<br><p align=right><a id="nuxt" href="#table-of-content">↩
Back To Top</a></p>

## [__Nuxt__]()

Nuxt is a progressive framework based on Vue.js to create modern web applications. It is based on Vue.js official libraries (vue, vue-router and vuex) and powerful development tools (webpack, Babel and PostCSS). Nuxt's goal is to make web development powerful and performant with a great developer experience in mind.

What is convenient with nuxt is that it sets up routing and [__server side rendering__](https://vuejs.org/v2/guide/ssr.html) ans [__static site generation__](https://medium.com/javascript-in-plain-english/generate-static-websites-with-nuxt-4fd0491340e) out-of-the-box. Most of this can be done in vue without nuxt but nuxt package and highly optimizes the files and save us a lot of overhead work.

<br><p align=right><a id="get-started-with-nuxt" href="#table-of-content">↩
Back To Top</a></p>

### [__Get started__]()
Nuxt can scaffold a project  with a predefined project file structure. Only requirement is to have node.js installed on your device. You scroffor a new project in new folder with a simple command. Read more [nuxtjs.org/guide](https://nuxtjs.org/guide/)
```javascript
> npx create-nuxt-app [project-name]
```
__Installation process__ described [nuxtjs.org/guide/installation](https://nuxtjs.org/guide/installation/)
```
options:

- choose name, description and author
- choose JavaScript or TypeScript (your prefered language) (default JavaScript)
- choose package manager (default Npm)
- choose UI framework module such as Bootstrap Vue, Bulma etc. (default none, recommended Bootstrap Vue)
- choose Server framework module such as Express, Koa etc (default none, recommended Express)
- choose additional nuxt modules such as detenv, axios etc (default none)
- choos linting tools such as ESLint, Prettier etc (default none, recommended ESLint)
- choose test framework jest, AVA (default none)
- choose application type universal (SSR - Server Side Rendered) or Single Page App (SPA) (default SSR)
- choose development tools. jsconfig.json is recommended and default.
```

To undestand the created __folder structure__ read __[here__](https://nuxtjs.org/guide/directory-structure/).

Note! You can always at later stage __change the configuration__ of you project.
- Project project name, description and author. In `package.json` file.
- Preferred language. In __???__
- Package manager. In __???__
- UI framework. In `package.json` file. Add/remove devDependencies  
- Application type. In nuxt.config.js file. Set mode to "universal","???" or "???". 


<br><p align=right><a id="structure-of-nuxt-projects" href="#table-of-content">↩
Back To Top</a></p>

### [__Structure of Nuxt projects__]()

@TODO

<br><p align=right><a id="basics-in-nuxt" href="#table-of-content">↩
Back To Top</a></p>

### [__Basics__]()

__<a id="attributes-vue">Attributes</a>__

[standard vue attributes...](TODO)

 
 

__Components:__  
Components can be imported in pages and layouts. Insted of importin header to each page is common to import i once to layout!
```javascript
import Header from './data/Header.vue'
import Header from '~components/data/Header.vue' // ~/@ refers to the root folder. Good for copy/paste
import Header from '@components/data/Header.vue' // ~/@ refers to the root folder. Good for copy/paste
```

__Pages:__  
This folder contains routes meaning pages that users can navigate to. 
The main default entry point is: 
```
index.vue
```
Then folder structure decides what possible routes are allowed. Pages are as normal components but with some extra functionality on topadded by nuxt. For example: validation.  


__Layouts__  
A main wraping element on the page. All pages and components can be wrapped in a ind of "frame" layout. A layout contain a tag `<nuxt></nuxt>` and this is the main "layout-frame" where all elements are loaded. The style in a layout defined in its <style></style> is unusually the main default style for the whole application (similar to css: [] in nuxt.config.js). 

We can add several the layouts in the `layouts` folder. Additional layouts (except default.vue)  must have extension .vue -  `[name].vue`. Then in each page that shall be loaded into this layout uses sa specialattribute in its `script-data`:  
```javascript
<script>
export default {
...
layout: '[name]',
...
```


__Error layout__   
It is a type of default layouot but with the reserved name  `error.vue`. If exist it will by default be used for all errors.

__Plugins__   
Here you can add any global .js programms that are run before the app is mounted. This make it possible to insert functionality that can be used globally such ass global components, filters, event-busses, variables etc


Following code demonstates how we can save time not needing to import components that are used almost everywhere. Create global component in a plugin that is run before main app instance is created. Then we can use the component in file templates withou importing and declarin those in out `<script>` parts.
```javascript
core-components.js
------------------

import Vue from "vue"

import AppButton from "@components/UI/AppButton"
import AppControlInput from "components/UI/AppControlInput"

Vue.component('AppButton', AppButton)
Vue.component('AppControlInput', AppControlInput)
```
```javascript
nuxt.config.js
--------------

...
plugins: [
  '~plugins/core-components.js' // must be added here
],
...

```

__Modules__  
Here you can add utility functions (Nuxt.js extensions extending the framework's core functionality) to our app that have been created by others. Nuxt can be extended with configuration options and plugins, but maintaining these customizations across multiple projects is tedious, repetitive and time-consuming. This is one of the reasons why Nuxt provides a higher-order module system that makes it easy to extend the core. A list of modules can be found [here](https://awesomejs.dev/for/nuxt/). If you want to read more deeply about what a module is check [here](https://nuxtjs.org/guide/modules/).

Adding a module is simple.
```
First instal npm package:
-------------------------

npm install -D bootstrap-vue
npm install -D @nuxtjs/axios
```
```
nuxt.config.js
--------------

...
modules: [
  // Doc: https://bootstrap-vue.js.org
  'bootstrap-vue/nuxt',

  // Doc: https://axios.nuxtjs.org/
  '@nuxtjs/axios',
],
...
```
Now you can use the extended bootsrtap and axios functionality globally in the app as descripbed in Deocumentation.

__Validation__  
`validate` shall be place in `script-data` part of page that receives the route and is called every time before navigation to a new route. It will be called server-side once (on the first request to the Nuxt app) and client-side when navigating to further routes. This method takes the context object as an argument.
```javascript
export default {
  ...
  validate ({ params, query, store }) {
    // Must be a number
    return /^\d+$/.test(params.id)
  }

  // or 

  export default {
    ...
    validate (data) {
      // Must be a number
      return /^\d+$/.test(data.params.id)
    }
  }
```


__Nested pages__  
Normally loaded pages takes up whole new screen. We can add a child "frame" where the output from the route is displayed. It is created by putting a `.vue` file in same directory as folder name similarly. Then routes from this "outer" vue file will be displayed in the index.vue frame defined inside the folder.

__Styling__  
Typically styling is `scoped` in pages, it only applies to elements in the page. Same applies to components. They usually contain `functional styling`. Application wide style is normally added in assest/styles folder and included in nuxt.config.js file. But each layout can contain non-scoped style appling to the layout as well. Therefore for app with multiple layout the method of including global main style from config file is recommended.

<br><p align=right><a id="routes-in-nuxt" href="#table-of-content">↩
Back To Top</a></p>

### [__Routes__]()

Folder structure with index.vue is recommended.
If folder name starts with `_[name]` then `[name]` is parameter name passed to child in:
```
$route.params.[name]
```

Example:
```
Folder structure
----------------

  /root
  - index.vue     <- main entry point
  - articles.vue  <- parent 
  /articles
    - index.vue   <-child (nested) frame
    /_aid
    - index.vue
```

```html
/root/articles.vue
-------------------
<template>
  <div>
    Enter article id:<input v-model="id">
    <button @click="$router.push('/articles/' + id)">Load id {{ id }}</button><br>
    <nuxt-link to="/articles/1">Link to is 1</nuxt-link><br>
    <nuxt-link to="/articles/2">Link to id 2</nuxt-link>

    <!-- Shoe routes in frame. Note style aplied from parent. -->
    <nuxt-child style="margin:50px; width: 300px; height: 150px; background-color: green;" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: null
    }
  }
}
</script>
```

```html
/root/articles/index.vue
-----------------------

<template>
  <div>
    <p>no article chosen</p>
  </div>
</template>
```

```html
articles/_aid/index.vue
-----------------------

<template>
  <div>
    <p>A single article with id {{ $route.params.aid }}</p>
  </div>
</template>

<script>
export default {
  validate(data) {
    const errorMsg = isNaN(data.params.aid) ? 'Invalid input. Not a number' : null
    // is not a number provided then false returned and page is "not found"
    return errorMsg == null
  }
}
</script>
```