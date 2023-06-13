# computed-property

In Vue 3, the Composition API is introduced as a new way to organize and reuse logic in Vue components. It allows you to define and use reactive state, computed properties, and methods in a more flexible and composition-friendly manner.

To use the Composition API, you need to create a new Vue component and define your logic inside the <script> tag with the lang="ts" attribute and setup() function. Here's an example of how you can define and use computed properties in Vue 3 using the Composition API:
  
```vue
<template>
  <div>
    <p>Computed Property: {{ fullName }}</p>
    <p>Reactive Property: {{ firstName }}</p>
  </div>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue';

// Define reactive properties
const firstName = ref('John');
const lastName = ref('Doe');

// Define a computed property
const fullName = computed(() => {
  return `${firstName.value} ${lastName.value}`;
});
</script>
```

In the example above, we import the necessary functions ref and computed from the Vue library. We then define two reactive properties, firstName and lastName, using the ref function. These properties can be used in the template, and their values can be updated reactively.

Next, we define a computed property called fullName using the computed function. The computed function takes a getter function as its argument, which returns the computed value. In this case, the getter function concatenates the firstName and lastName values to form the full name.

The computed property fullName can be used in the template just like any other property, and it will automatically update whenever the dependent reactive properties (firstName or lastName) change.

Note that you'll need to have Vue 3 and the Vue Composition API plugin installed to use the Composition API in your project.  
  
## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
