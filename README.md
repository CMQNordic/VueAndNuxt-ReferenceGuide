## ___Vue.js and Nuxt -&nbsp;Ultimate&nbsp;Reference&nbsp;Guide&nbsp;-___
---
By&nbsp;Martin&nbsp;Czerwinski @ [CMQ&nbsp;Nordic&nbsp;AB](www.cmq.se "www.cmq.se (Martin Czerwinski @ CMQ Nordic AB)") &nbsp;March&nbsp;2020&nbsp;®

---

__Vue.js__ is a modern open source java script  is a progressive framework for building front end user interfaces and single-page applications. 

__Nuxt__ is ...

Bookmark this page, share it and feel free to [__reach out to us__](www.cmq.se "Contact us!") with questions, comments or requests for assignments!

---

#### __TABLE OF CONTENT__

  - [__1. Vue.js__](#vue-js) 
    - [Progressive vs monolithic frameworks](#progressive-vs-monolithic)
	- [Single page vs Universal projects](#ssp-vs-universal)
	- [Vue vs React vs Angular](#vue-vs-react-angular)
    - [Basics of Vue.js](#basic-of-vue)<br>
  	[Directives](#directives-in-vue) ◦ [XXX](#import-data-into-a-query-in-m) ◦ [XXX](#types-values-in-m)
	- [DDD](#basic-of-vue)<br>
	[XXX](#basics-of-m) ◦ [XXX](#import-data-into-a-query-in-m) ◦ [XXX](#types-values-in-m)

  - [__2. Nuxt__](#vue-js) 
    - [AAA](#progressive-vs-monolithic)
	- [BBB](#ssp-vs-universal)
    - [CCC](#basic-of-vue)<br>
  	[XXX](#basics-of-m) ◦ [XXX](#import-data-into-a-query-in-m) ◦ [XXX](#types-values-in-m)
	- DDD](#basic-of-vue)<br>
	[XXX](#basics-of-m) ◦ [XXX](#import-data-into-a-query-in-m) ◦ [XXX](#types-values-in-m)


<br>

## __[1. Vue.js]()__

<br><p align=right><a id="progressive-vs-monolithic" href="#table-of-content">↩ Back To Top</a></p>
#### [Progressive vs monolithic frameworks]()
---
When you're developing in Node.js, you're likely to run into these terms - "monolithic" and "modular" or "progressive". They're usually used to describe the different types of frameworks and libraries; not just HTTP frameworks, but modules in general.

Vue.js in an example of progressive framework. The word "progressive" means whole framework and progressively add more parts and functionality of it e.g. the view functionality, outer or vuex can be added to it. Only includes the bare minimum of functionality and structure, and the rest is a plugin.

Monolithic frameworks are typically tightly coupled, trying to include all the stuff that's needed for common use-cases. An example of a monolithic web framework would be Sails.js.

At first, a monolithic framework might look easier - after all, it already includes everything you think you're going to need. In the long run, however, you're likely to run into situations where the framework just doesn't quite work how you want it to, and you have to spend time trying to work around it. This problem gets worse if your usecase is more unusual - because the framework developers didn't keep in mind your usecase - but it's a risk that always exists to some degree.

Initially, a modular framework might look harder - you have to figure out what components to use for yourself. That's a one-time cost, however; the majority of modules are reusable across projects, so after your first project you'll have a good idea of what to start with. The remaining usecase-specific modules would've been just as much of a problem in a monolithic framework, where they likely wouldn't have existed to begin with.

<br><p align=right><a id="ssp-vs-universal" href="#table-of-content">↩ Back To Top</a></p>
#### [Single page vs Universal projects]()
---
Web applications are unwittingly replacing the old desktop applications. They are more convenient to use, they are easy to update, and they are not bound to one device. There are two main design patterns for web apps: multi-page application (MPA) and single-page application (SPA). And of course, both models have their pros and cons.

What content do you want to present and what content your users will care about the most?

A single-page application is an app that works inside a browser and does not require page reloading during use. Examples: Gmail, Google Maps, Facebook or GitHub. SPAs are all about serving an outstanding UX by trying to imitate a “natural” environment in the browser — no page reloads, no extra wait time. It is just one web page that you visit which then loads all other content using JavaScript — which they heavily depend on.

SPA are fast. The development is simplified and streamlined. There is no need to write code to render pages on the server. It is much easier to get started because you can usually kick off development from a file file://URI, without using any server at all. SPAs are easy to debug with Chrome, as you can monitor network operations, investigate page elements and data associated with it. It’s easier to make a mobile application because the developer can reuse the same backend code for web application and native mobile application. 

Cons: It is very tricky and not an easy task to make SEO optimization of a Single-Page Application. It need to download heavy client frameworks are required to be loaded to the client. It requires JavaScript to be present and enabled but due to recent server side rendering techniques you can render the page on the server already. 



<br><p align=right><a id="vue-vs-react-angular" href="#table-of-content">↩ Back To Top</a></p>
#### [Vue vs React vs Angular]()
---

React and angular have been popular frameworks
from a few past years. React is released in 2013 by Facebook. It is mostly used in high traffic websites. Whatsapp, Instagram Paypal, Glassdoor, BBC are some of the popular companies using React.

A progressive Javascript framework released in 2014 and developed by no
big name like React and Angular.It is the youngest member of the family of Javascript frameworks. It has practically removed the drawbacks of the other frameworks to offer ease
of next level to software developers. Websites like GitLab and Alibaba
are using Vue.

Released in 2010 by Google. It is a typescript based javascript framework. It
was released prior to the other two Javascript frameworks. Google and Wix are among the most popular companies using Angular.


There is a thing called DOM which can be understood as UI, that is the user
interface of your application. The DOM changes whenever you update the
user interface. This represents the changes that are made in the
application. It can be used in two ways, either as virtual DOM or a real DOM. The performance of the framework/library is highly affected by them. 

Angular: This framework of Javascript uses real DOM. It is extremely hard to handle
because if you lose the flow, you will have to go deep into the codes to
actually find out the issue. It also might results in bit slower
performance of this Javascript framework.

React: This framework is using virtual DOM. It is not browser specific and
lightweight. It is provided in react package for free and eliminates
the issues of slow performance of real DOM. Significant improvement in the performance of javascript frameworks/ libraries and made React utterly popular.

Vue has taken all the good attributes of frameworks launched before it.
With the same concept, Vue is using Virtual DOM as an adopted concept of
React. This ensures faster and bug-free performance.

Vue is the lightest of all. Vue and React are suitable for light-weight application whereas Angular for heavyweight application.

Vue and React do not require to hire web developers who are proficient in typescript. But among these two, Vue has an upper hand as it is considered more friendly by the developers.
 Angular is diminishing in popularity.

Vue and React offers better performance and flexibility than Angular.
Vue and react are more suited for light-weight applications and angular is the best for large UI applications.
Angular is highly opinionated and unlike Vue and React, it offers everything
from routing, templates to testing utilities in its package.
Vue is the most popular, loved and growing framework of Javascript.



<br><p align=right><a id="basic-of-vue" href="#table-of-content">↩ Back To Top</a></p>
#### [Basics of Vue.js]()
---

Vue.js is a system that enables us to render DOM data using straightforward HTML template syntax and bind DOm and Template to each other:

Vue.js API [here](https://vuejs.org/v2/api/)

![Basic Vue syntax](assets\images\basic_example.JPG)

__HTML__
```html
	<div id="app">
		Name:<input v-model="name">
		<button @click="age++">Increase age</button>
		<p> My name is <span :class="{visible: name.length<=0}">{{ name }}</span> and I am {{ age }} years.</p>
		<p> Name and age are: {{ getName }} | {{ getAge() }}</p>
	</div>
```
__Javascript__
```javascript
var vm = new Vue({
	el: '#app',
	data: {
		name: '',
		age: null,
	},
	computed: {
		getName: function () { return this.name }
	},
	methods: {
		getAge: function () { return this.age }
	},
	watch: {
		age: function () {
			(this.age == 3 || this.age == 6) ? alert('age is now ' + this.age) : null
		}
	}
})
```
__CSS__
```css
<style>
	.visible {
		display: inline-block;
		height: 18px;
		width: 40px;
		background-color: lightgrey;
		border: 1px dotted black;
	}
</style>
```

__`el`__ - Id in HTML to refer toward witch this vue instance data refers to.<br>
__`data`__ - Variables/properties storing data. Data is not reactive. No calculations possible here.<br>
__`computed`__ - Properties/functions that is executed ONLY when variables they depend on are affected.<br>
__`methods`__ - Functions that are executed when called.<br>
__`watch`__ - Methods that are executed only if a computed or data property change.<br>

__Vue.js__ instance, created by constructor `vm1 = new Vue({})` takes parameters like data or methods and proxies those to be part of view object. We can  access those by calling vm1.<parameters>. We can access this vm1 object from other instances or normal java script functions.

Reach this in vue instance and outside. To reach this properties outside vue instance use __`$this`__.

Properties in Vue instance starting with $ are the native vuejs objects we can access.: 
__$el__: el object in constructor -
__$data__: the data object in constructor - vm1.$data.<property>

__$refs__: The `ref` that we can set on each HTML element to refer to it. Note that using $refs is not recommended for setting DOm elements as Vue template when render will overwrite it. Still it is good to use $ref for accessing native elements in DOM. Example: 
```
<button ref=""MyButton>Press</button>
vm1.$refs.MyButton.InnerText="Press me"
```

![Vue instance lifecycle](assets\images\instance_lifecycly.jpg)

__Computed vs Method.__ In example above when "Increase Counter" is pressed both `getCounterByComputed` and `getCounterByMethod` functions are executed - as expected. But when "Increase Dummy" is pressed only `getCounterByMethod` is executed. This because Vue checks if a computed function has dependency to any data property that changed before running the function. Here not, as dummy is not used in `getCounterByMethod` function, therefore no need to run this function. Performance saver! 

__Classes and CSS.__ there are two ways to bind the class (css style) to an HTML object.

Examples:<br>
```html
<div  class="some-class" v-bind:class=['<class-name1>', '<class-name2>'] ></div>

<div class="some-class" :class={<class-name1>: true, <class-name2>: true} ></div>
```
Vue will concatenate the classes, those defined normally by class and those through are bound to vue with v-bind.
Key/Value pairs are objects where value is boolean and if true then the class is applied.


<br><p align=right><a id="CLI-in-vue" href="#table-of-content">↩ Back To Top</a></p>
#### [Vue CLI]()

![Vue CLI](assets\images\vue_cli.JPG)

<br><p align=right><a id="directives-in-vue" href="#table-of-content">↩ Back To Top</a></p>
#### [Directives]()
---

The v-bind attribute you are see in HTML is called a directive. Directives are prefixed with v- to indicate that they are special attributes provided and executed by Vue and they apply special reactive behavior to the rendered DOM.

DOM event objects [here](https://www.w3schools.com/jsref/dom_obj_event.asp)<br>
Event handling in Vue.js [here](https://vuejs.org/v2/guide/events)
Event modifiers in Vue.js [here](https://vuejs.org/v2/guide/events.html#Event-Modifiers)

||||
|---|---|---|
|`{{ }}`| Text interpolation. Adds Data property as text into HTML template |`<p>My name is {{name}}</p>`|
|`v-bind:<attribute>`<br>`=<data>`<br>or<br>`:<attribute>=<data>`| One way binding. Binds Data property to HTML attribute |`<img v-bind:src="image">` or shortly `<img :src="image">`|
|`v-model="<data>"`| Two way binding. Binds Data property to HTML field and at same time if changed then back to Data model. All instances used of the property will update. |`<input v-model:"name"><p>{{ name }}</p>`|
|`v-on:<event>`<br>or<br> `@<event>`| Sends own param and/or event from HTML template to Data |`<button v-on:keydown ="keyDown(2, $event)">Click me<button>` or short `<button @keydown ="keyDown(2, $event)">Click me<button>`|
|`@<event>.stop`| Stops the bubbling of an event to parent elements, `stopPropagation()`. Use prevent for `preventDefault()`. Event modifiers [here](https://vuejs.org/v2/guide/events.html#Event-Modifiers) |`<button @click.stop">Click me<button>` |
|`@<key-event>.enter.space`| Trigger event function only for `enter` & `space` keys. Event modifiers [here](https://vuejs.org/v2/guide/events.html#Event-Modifiers) |`<input @keyup.enter.space ="func">` |
|`v-if:"true/false"`| Binding visibility of element to Data property|`<span v-if:"bVisible">Visible or not</span>`|
|`v-for="i in <array>"`|Display list of items based on Array in Data| `<ol><li v-for="i in arrayX">{{ i.text }}</li></ol>` |

