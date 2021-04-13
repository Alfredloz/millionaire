<template>
  <div id="app" class="d_flex">
    <img alt="Vue logo" src="./assets/million-logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <MillionComponent/>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MillionComponent from './components/MillionComponent.vue'

export default {
  name: 'App',
  components: {
    MillionComponent,
  }
}
</script>

