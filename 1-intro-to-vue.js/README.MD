## Intro to Vue.JS

### Vue Instance

* new Vue({ options }) - new vue instance
* root of vue appln
* like heart of the appln which powers everything
* el property is used to plug it to html element
* data property has data values for that instance
* {{ }} - Expression -- used to produce or evaluate data
* Vue is Reactive in nature

### Attribute binding

* v-bind:attribute="expression"
* dynamically binds an attribute to an expression
* shorthand --> use only colon like :alt, :href

### Conditional Rendering

* v-if="expression"
* v-else-if
* v-else
* the above will add and remove elements from DOM
* v-show, v-hide --> toggles visibility of element

### List Rendering

* v-for="item in items" --> items is array
* use :key attribute to keep track of node's indentity

### Event Handling

* v-on:event="expression/methods"
* shorthand --> @click, @mouseover
* @submit, @click, 
* @keyup.enter - .enter is event modifier

### Class and Style Binding

* :style="{ property: value/expression }"
* :style="styleObject"
* :style="[styleObject, styleObject2]"
* :class="{ className: expressionValue(true/false) }"
* can add ternary expression too

### Computed Properties

* kind of like methods which depends on data values
* runs everytime its dependency is changed

### Components

* reusable block of code which gives us modular and maintainable codebase
* fit together to create app
* register component - Vue.component(name, {
    props: { // or use props array without validation
        message: {
            type: String,
            required: true,
            default: 'hi'
        }
    },
    template: `Elements`, // should contain exactly one root element
    data() {
        return { // returns a fresh data object for each component

        }
    }
* })
* props - a custom attribute for passing data to components
* Communicating events between components(parent-child)
  * this.$emit(eventname) in child
  * @eventname="function" in parent

### Forms and 2 way data binding

* v-model="data" -- update data both ways

### EventBus

* global bus which all components have access to