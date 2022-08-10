<template>
  <section class="container">
    <h2>See Console</h2>
  </section>
</template>

<script setup>
import { watch, ref } from 'vue';

//// 1. Watching a single ref ////
// const name = ref('Jay');

// watch(name, (currentValue, oldValue) => {
//   console.log(oldValue);
//   console.log(currentValue);
// });

// setTimeout(function () {
//   name.value = 'Max';
// }, 2000);

//// 2. Watching multiple ref's ////
// const firstName = ref('Jay');
// const lastName = ref('Pritchett');
// watch([firstName, lastName], (currentValue, oldValue) => {
//   console.log(oldValue);
//   console.log(currentValue);
// });

// setTimeout(function () {
//   firstName.value = 'Ali';
//   lastName.value = 'kamal';
// }, 2000);

//// 3. Watching a ref array ////
// const level = ref([1, 2, 3, 4]);

// watch(
//   () => [...level.value],
//   (currentValue, oldValue) => {
//     console.log(oldValue);
//     console.log(currentValue);
//   }
// );

// console.log(level.value);

// setTimeout(function () {
//   level.value.push(15);
// }, 2000);

//// 4. Watching a ref array ////
const state = ref({
  name: 'Said',
});

console.log(state.value);

watch(state.value, (currentValue, oldValue) => {
  console.log(oldValue);
  console.log(currentValue);
});

setTimeout(function () {
  state.value.name = 'Kamal';
}, 2000);
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

.container {
  margin: 3rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  text-align: center;
}
</style>
