# first-project

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
###differents between ref and reactive state on rectivity fundamentals

In Vue.js 3, both ref and reactive state (reactive) are used for managing reactive data. They both provide a way to create reactive data that triggers updates to the user interface when the data changes. However, there are some key differences between the two:

ref:

. ref is a function provided by Vue.js that creates a reactive reference to a value.
. When you create a ref, it wraps the value in a special object, and the reactive behavior is achieved through this wrapper.
. To access the underlying value of a ref, you need to use the .value property.
. t is commonly used for simple values like numbers, strings, or objects that don't require deep reactivity.

```sh
import { ref } from 'vue';

const count = ref(0);

// To access the value, use .value property
console.log(count.value); // 0

// Updating the value will trigger reactivity
count.value += 1;

```
2.Reactive state (reactive):

.reactive is another function provided by Vue.js that creates a fully reactive proxy of an object.
.When you create a reactive state with reactive, the entire object becomes reactive, including all its properties and nested properties.
.There's no need to use .value to access the properties; you can directly access them like a regular JavaScript object.
.It is suitable for more complex data structures like nested objects or arrays that require deep reactivity.

```sh
import { reactive } from 'vue';

const user = reactive({
  name: 'John',
  age: 30,
  address: {
    city: 'New York',
    country: 'USA'
  }
});

// Accessing properties directly without .value
console.log(user.name); // 'John'
console.log(user.address.city); // 'New York'

// Changing properties triggers reactivity
user.age += 1;
user.address.city = 'San Francisco';


```
