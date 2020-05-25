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
    - [Progressive vs Monolithic frameworks](#progressive-vs-monolithic) ◦ [Single page vs Universal projects](#ssp-vs-universal) ◦ [Vue vs React vs Angular](#vue-vs-react-angular)
    - [Install Vue & Start new project](#installing-vue)
    - [Basics of Vue.js](#basic-of-vue)
    - [Custom events](#components-communication-in-vue)
    - [Single-file components](#single-file-components-in-vue)
    - [Slots & Components](#slots-and-components-in-vue)
  	- [Directives](#directives-in-vue)
	- [XXX](#basics-of-m) ◦ [XXX](#import-data-into-a-query-in-m) ◦ [XXX](#types-values-in-m)

  - [__2. Nuxt__](#vue-js) 
    - [AAA](#progressive-vs-monolithic)
	- [BBB](#ssp-vs-universal)

<br>

## __[1. Vue.js]()__

<br><p align=right><a id="progressive-vs-monolithic" href="#table-of-content">↩ Back To Top</a></p>
### [__Progressive vs Monolithic frameworks__]()
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

### [__Vue vs React vs Angular__]()
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


<br><p align=right><a id="installing-vue" href="#table-of-content">↩ Back To Top</a></p>

### [__Install Vue & Start new project__]()
---

Vue provides an official CLI (Command Line Interface) vue-cli that mainly has one major task and that is helping to quickly scaffold (autogenerate) templates for new Vue application projects. It provides build setups for a modern frontend workflow based on several templates, wizards and settings. with it you can get started easily with hot-reload, lint-on-save, and production-ready builds.  NPM is the recommended as the installation method when building large scale applications with Vue. Vue pairs very well with webpack package manager. To check your current version run in command window `vue --version`

Detailed Vue installation guide can be found [here](https://vuejs.org/v2/guide/installation.html).<br>
Detailed VUE-CLI installation guide can be found [here](https://cli.vuejs.org/guide/installation.html).

An _nmp package_ should be installed globally when it provides an executable command that you run from the shell (CLI), and it’s reused across projects. Some packages are just better installed globally and npm, gatsby-cli or vue-cli are some of them.

Following command installs vue and vue-cli:<br>
> __`npm install vue`__ -> vue only<br>
> __`npm install -g @vue/cli`__ -> vue & cli<br>

After installation you will have access to the vue binary in your command line. Run `vue` command to check if installation was ok.

_Note!<br> 
Up to vue-cli v.2 we used `vue init` command with chosen project template (i.e.webpack, webpack-simple, browserify, simple m.m.). In vue -cli v.3 this has been changed and the project is now initiated by `vue create` command following a wizard, or from GUI by command `vue ui`._

__Start and scaffold new project__<br>
> __`vue ui`__ -> start new project from GUI<br>
> or<br>
> __`vue create <project-name>`__ -> follow command wizard with many configuration options

If you still need the legacy `vue init` functionality, you can install a global bridge.<br>
A light template for simple prototyping named `webpack-simple` can be used.<br><br>
> __`npm install -g @vue/cli-init`__<br>
> __`vue init webpack-simple <your-project-name>`__

Note!<br>
If absolute path to <you-project-name> contains & characters you might experience strange error when running webpack-dev-server. Avoid & characters in you folder names in run project. 

<br><p align=right><a id="basic-of-vue" href="#table-of-content">↩ Back To Top</a></p>

### [__Basics of Vue.js__]()
---
[Attributes](#attributes-vue) 
◦ [Instances](#vue-instance-vue) 
◦ [Components](#components-vue) 
◦ [Computed vs Method](#computed-vs-method-vue)
◦ [Event modifiers](#event-modifies-vue)
◦ [Key modifiers](#key-modifies-vue)
◦ [Props](#props-vue)
◦ [Native properties in this](#native-properties-in-vue)
◦ [Classes and Styles](#classes-and-style-in-vue)
◦ [Life-hooks](#life-hooks-in-vue)

Vue.js is a system that enables us to render DOM data using straightforward HTML template syntax and bind virtual DOM and Template to each other.

Vue.js API can be found [here](https://vuejs.org/v2/api/). Following example [on jsfiddle](https://jsfiddle.net/martin_cmq_nordic/ch64syad/3/)

__<a id="basic-example-of-vue">Basic example.</a>__

![Basic Vue syntax](assets\images\basic_example.JPG)

__HTML__
```html
<h1>APP1</h1>
<div id="app1">
	Name:<input v-model="name"><button @click="age++">Increase age</button>
	<p> My name is <span :class="{'visible-empty': (name.length <= 0)}">{{ name }}</span></p>
	<p> I am <span :class="{'visible-empty': (age <= 0)}">{{ age }}</span> years old.</p>
	<p> {{ getName }} | {{ getAge() }}</p>
</div>

<h1>APP2</h1>
<div id="app2"></div>

<h1>APP3</h1>
<div id="app3">
	<my-local-component :type="'Local'"></my-local-component>
	<my-global-component :type="'Global'"></my-global-component>
</div>

<h1>APP4</h1>
<div id="app4">
	<my-local-component :type="'Local'"></my-local-component>
	<my-global-component :type="'Global'"></my-global-component>
</div>
```
__JAVASCRIPT__
```javascript
<script>
	var vm1 = new Vue({
		el: '#app1',
		data: {
			name: '',
			age: null
		},
		computed: {
			getName: function () {
				return this.name
			}
		},
		methods: {
			getAge: function () {
				return this.age
			}
		},
		watch: {
			age: function () {
				(this.age == 3 || this.age == 6) ? alert('Age is now ' + this.age) : ''
			}
		}
	})

	var vm2 = new Vue({
		el: '#app2',
		computed: {
			// We can not access vm1 direct from template. Must go though computed attribute
			getAgeFromApp1: function () {
				return vm1.age
			}
		},
		methods: {
			onEvent: function (age, event) {
				vm1.age = (age>0)?age:vm1.age;
				console.log(event.type);
				console.log(this.$refs);
				this.$refs.typeText.innerText = 'Event type: ' + event.type;
			}
		},
		mounted: function() {
			// change the text of button with help of ref
			// template have not set $refs until mounted
			this.$refs.myButton.innerText = 'Click to set age to 23 in app1';
			
		},
		template: '<div>
			     		<button @click="onEvent(23, $event)" @mouseover="onEvent(0, $event)" ref="myButton">
						</button>
						<p ref="typeText"></p>
						Age in app1 is {{ getAgeFromApp1 }}
				   </div>'
	})

	// simple component definition with template. note data is here a function.
	var cmp = {
		data: function() {
			return { number: 5 }
		},
		// props define parameters sent down to the component from parent
		props: ['type'],
		template: '<div>{{type}}. Number {{ number }} <button @click="number+=1">Increase</button></div>'
	}

	// Following component definition can work very well for small to medium-sized projects, 
	// where JavaScript is only used to enhance certain views. 
	// In more complex projects however, single-file components with a .vue extension
	// should be used together with build tools such as Webpack or Browserify.

	// Global component definition
	Vue.component('my-global-component', cmp );

	var app3 = new Vue({
		el:'#app3',
		// local component definition
		components: {
			'my-local-component': cmp,
		}
	})

	var app4 = new Vue({
		el:'#app4'
	})
</script>
```
__CSS__
```css
<style>
	.visible-empty {
		display: inline-block;
		height: 18px;
		width: 40px;
		border: 1px dotted black;
	}
</style>
```
__<a id="attributes-vue">Attributes.</a>__
> __`el`__ - Identification of HTML element to refer to for this application.<br>
> __`data`__ - Variables/properties storing non reactive data. No calculations possible here. Note! If defined in single file template then this must be a function returning an object<br>
> __`computed`__ - Properties/functions that is recalculated/executed ONLY when variables they depend on are changed.<br>
> __`methods`__ - Functions that can be called for execution.<br>
> __`watch`__ - Methods that are executed only if a computed or data property change.<br>
> __`props`__ - Data passed to a child component where it then is available as a property.<br>
> __`mounted`__ - instance life-cycle hook. In the mounted hook, you will have full access to the reactive component, templates, and rendered DOM (via. this.$el)

__<a id="vue-instance-vue">Vue.js instances.</a>__<br> 
Created by `const vm = new Vue({})` takes an object with parameters like data or methods as input. We can  access those by calling `vm.<parameters>`. We can access this `vm` object from other instances or normal java script functions.

__<a id="components-vue">Components.</a>__<br> 
Vue components is an extension of an instance. Given a name it can be reused in the instance root several times. This is the main building block together with instance of an Vue application.

Naming can be as _kebab-case_ `my-component-name` or _PascalCase_ . When defining a component with PascalCase, you can use either case when referencing its custom elements.

Components can be registered globally and accessed within all children:<br>
`Vue.component('my-component-name', { /* ...template... */ })`<br>
or locally within the instance only to access in this instance:
```javascript
<script>
// If using ES2015 modules, such as through Babel & Webpack
// That might look more like:
import componentY from './ComponentY.vue'
var componentX = { /* ...template... */ }


new Vue({
  el: '#app',
  components: {
    'component-x': componentX,
    'ComponentY': componentY
  }
})
<template>
```

__<a id="computed-vs-method-vue">Computed vs Method.</a>__<br> 
In example above when "Increase Counter" is pressed both `getCounterByComputed` and `getCounterByMethod` functions are executed - as expected. But when "Increase Dummy" is pressed only `getCounterByMethod` is executed. This because Vue checks if a computed function has dependency to any data property that changed before running the function. Here not, as dummy is not used in `getCounterByMethod` function, therefore no need to run this function. Performance saver! 

__<a id="event-modifies-vue">Event modifiers.</a>__<br>
Event can be modified to do different things when cached. Here for example do `event.stopPropagation()` by simply adding `stop` after event as below. Read about more types of modifiers [here](https://vuejs.org/v2/guide/events.html#Event-Modifiers). <br> 
`<span @mousemove.stop=""></span>`

__<a id="key-modifies-vue">Key modifiers.</a>__<br>
For key-events we can bind certain keys to react for. Here for example execute alert function only when `enter key` was pressed.<br><br>
`<input @keyup.enter="alert('enter pressed')">`


__<a id="props-vue">Props.</a>__<br>
Props are properties set from outside and passed into the component. Props can be of primitive or reference type. Props in component be set as simple array of names, or with validation. Validation of props is good to use as we get warnings in console at dev time when we send to a component something a datatype we do not expect. 

When sending _primitive types_ like String or Number into a component the memory is copied and changes to property inside the component are not visible outside. But note that when mutating such a prop the value in the component will be overwritten whenever the parent component re-renders. 

When sending _reference types_ like Function, Array or Object as a prop to a component then only the pointer to the memory is sent and the component do not "owe" the property. The changes to this property (or function call) within the component will be visible outside.Example:
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
Properties in __`this`__ (Vue instance struct) starting with `$` are the native vue objects we can access.<br>


__`$el`__: el object in constructor to be reached through this<br>

__`$data`__: the data object in constructor to reach properties with `this.$data.<property-name>`

__`$refs`__: The `ref` that we can set on any HTML element to refer to it easily. Note that using  this is not recommended for setting DOM elements as Vue template when rendered will overwrite those. It is good to use `this.$refs.<ref>` for accessing native elements in DOM. 

Example: 
```html
HTML
<button ref="myButton"></button>

SCRIPT
this.$refs.myButton.InnerText="Press Me"

// Note! to reach a ref an instance the life-hook mounted() to DOM shall be executed in order for all refs to be set.
```

__<a id="classes-and-style-in-vue">Classes and Styles.</a>__<br> 
There are two ways to bind the class or css style to an HTML object. Vue will concatenate the classes - those defined normally by class with those through bound with are v-bind.
```html
// Class bound as an array of class names
<div class="some-class" :class=['className1', 'className2']></div>

// Class bound as key/value objects where key is either true/false deciding if this class shall be enabled or not.
<div class="some-class" :class={'class-Name1': true, className2: false}></div>
```
__<a id="life-hooks-in-vue">Life-hooks.</a>__<br> 
Read more here about understanding [Vue.js Lifecycle Hooks](https://www.digitalocean.com/community/tutorials/vuejs-component-lifecycle)
![Vue instance lifecycle](assets\images\instance_lifecycly.jpg)

Instance life cycle can be reached by:<br>
```javascript
mounted: function() {
	this.$refs.myButton.innerText = 'Set age to 23 in app1';
},
```

<br><p align=right><a id="components-communication-in-vue" href="#table-of-content">↩ Back To Top</a></p>

### [__Custom events__]()
---
[Parent->Child](#parent-child-communication) ◦ [Child->Parent](#child-parent-communication) ◦ [Component<->Component](#component-component-communication)


__<a id="parent-child-communication">Parent -> Child</a>__ (setting `props`)<br>


```html
When sending String or Number into a component the memory is copied and changes to property inside the component are not visible outside. But note that when mutating such a prop the value in the component will be overwritten whenever the parent component re-renders. 

When sending Function, Array or Object as a prop to a component then only the pointer to the memory is sent and the component do not "owe" the property. The changes to this property (or function call) within the component will be visible outside.

_____________PARENT_________________
<!-- Sending probs down to child -->
<child-component :id="2" :name="'Martin'"></child-component>

<script>
	import Child from './ChildComponent.vue';

	export default {
		components: {
			'child-component': Child
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
				required: true
			},
			name: {
				type: String,
				default: 'undefined'
			},
		}
	}
</script>
```

__<a id="child-parent-communication">Child -> Parent</a>__ (`$emit` events)
```html
Child component can emit (trig) an custom event upward to parent with event data.
This method can not be used to send data to other child components. Must then go though parent.

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

_____________PARENT_________________
<!-- Parent listens to emitted event and reads $event data -->
<template>
	<p>{{ name }}</p> 
	<child-component @eventFromChild="name=$event.name"></child-component>
</template>
```

__<a id="component-component-communication">Component <-> Component</a>__ (emit on `eventBus` instance)
```html
_____________main.js____________
<!-- export new empty vue instance from script -->
export const appEventBus = new Vue();

_______Component Sender_________
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

<br><p align=right><a id="single-file-components-in-vue" href="#table-of-content">↩ Back To Top</a></p>

### [__Single-file components__]()
---
__Components__ extend _Vue instances_ and are reusable in other components. We can use components as a custom element. Components can be declared __globally__ or __locally__ in an instance. In more complex projects single-file components (with a .vue extension) should be used together with build tools such as Webpack or Browserify that auto-generate javascript that is served to browser. 

When using vue-cli to start project a project template with auto-generated configuration is set up for you. `Webpack.config.js` file defines tools and bundles all our files to one build.js that is serves to the browser. `Package.json` file define packages to use and scripts to run. 

Simple project based on single-file template can look like this:<br>
Here we have a Parent instance defining 3 components and using those as children (2 `ClickCounter` components and 1 `Logs`). Parent send __`props`__ to children and on eof those is a callback function that children directly can execute. Both `ClickCounter` children __`emit`__ even up to parent telling about changes. All components are sending log events on the __`eventBus`__ and Logs component is listening to those and viewing the logs.

__This example__ demonstrates structure of an vue application using single-file templates and communication between parent, children and between components.

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

import Vue from 'vue'
import App from './App.vue'

export const appEventBus = new Vue();

new Vue({
  el: '#app',
  render: h => h(App)
})
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
    <app-click-counter  :compName="'A'" 
                        :counter="counterA"
                        :resetAllCB="resetAll" 
                        @counterChanged="counterA=$event">
    </app-click-counter>
    <app-click-counter  :compName="'B'" 
                        :counter="counterB" 
                        :resetAllCB="resetAll" 
                        @counterChanged="counterB=$event">
    </app-click-counter>
    <app-logs></app-logs>
  </div>
</template>

<script>
import ClickCounter from "./Components/Temp/ClickCounter.vue";
import Logs from './components/Temp/Logs.vue';

// Parent need to send event on the bus (that log listens to)
import { appEventBus } from "./main";

export default {
  // local components used from withing here
  components: {
    'app-click-counter': ClickCounter,
    'app-logs': Logs
  },
  data: function() {
    return {
      counterA: 0,
      counterB: 0
    }
  },
  computed: {
    getAllCounters() {
      return ' Counters: A=' + this.counterA + ' B=' + this.counterB;
    }
  },
methods: {
    resetAll() {
		this.counterA = 0;
		this.counterB = 0;
	
		// Send event on the bus to those who listen
		appEventBus.$emit('logEvent', {
			source: 'Parent',
			text:'resetAll() executed. All counters set to 0.'
		})
    }
  }
}
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
    <button @click="increaseCounter(1)">You clicked here {{ counter }} times</button>
    <button @click="increaseCounter(null)">Reset this</button>
	<!-- when clicked call a callback in the parent that resets all counters -->
	<button @click="resetAllCB()">Reset all</button>
    <p v-if="counter > 0">{{  "Counter: " + counter }}</p>
  </div>
</template>

<script>
import { appEventBus } from "../../main";

export default {
  props: {
	  compName: {
		  type: String,
		  required: true
	  },
	  // mutated prop, can be overwriten from parent
	  counter: {
		  type: Number,
		  required: true
	  },
	  // callback that resets the mutated counter
	  resetAllCB: {
		  type: Function,
		  required: true
	  }
  },
  methods: {
	  increaseCounter(value) {
		  if (value  == null)
		  {
			this.counter = 0;
		  } 
		  else 
		  {
			  this.counter += value;
		  }
		  
		  // emit an event up to parten informing about counter change
		  this.$emit('counterChanged', this.counter);
		  
		  // Send log event on the bus to those who listen
		  appEventBus.$emit('logEvent', {
			  source: this.compName,
			  text:'Counter increased to ' + this.counter
		  })
	  }
  }
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
import { appEventBus } from "../../main";

export default {
  data: function() {
    return {
      compName: "Logs",
      logs: []
    };
  },
  // when created (life-hhok) set listener to log events
  created() {
    appEventBus.$on("logEvent", (log) => {
      this.logs.push(log);
    });
  }
};
</script>

<style>
.log {
  background-color: white;
  padding: 3px;
}
</style>
```


<br><p align=right><a id="slots-and-components-in-vue" href="#table-of-content">↩ Back To Top</a></p>

### [__Slots & Dynamic Components__]()
---
Slots help you distribute code in other components. Good to build reusable widgets like a slideshow.
A template can contain a named slot that can be dynamically modified from outside. Default content in single-file template slot can be added and it is shown until the slot is not used/filled with content.

Note that parent is rendering both style and text before from outside the template (style rendering from the child itself is possible too)
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

<br><p align=right><a id="directives-in-vue" href="#table-of-content">↩ Back To Top</a></p>

### [__Directives__]()
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


