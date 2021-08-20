<template>
  <div id="app">
    <app-tabs/>
   
  </div>
</template>

<script>
import AppTabs from './components/AppTabs.vue'


export default {
  name: 'App',
  components: {
    AppTabs,
  }
}
</script>

<style>
#app {
 background: rgb(114, 113, 113);
}
</style>
