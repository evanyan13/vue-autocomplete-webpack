<template>
    <div>
      <h1>Hello Vue 2 with Webpack!</h1>
      <AutocompleteBundledUi />
    </div>
  </template>
  
  <script>
  import AutocompleteBundledUi from './components/AutocompleteBundledUi.vue';

  export default {
    name: 'App',
    components: {
      AutocompleteBundledUi
    }
  };
  </script>
  
  <style>
  h1 {
    color: #42b983;
  }
  </style>
  