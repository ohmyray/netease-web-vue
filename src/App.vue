<template>
  <div class="nav-top">
    <div class="container nav">
      <NavBar></NavBar>
    </div>
  </div>
  <div class="container">
    <HelloWorld msg="Hello Vue 3 + TypeScript + Vite" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import NavBar from './components/NavBar.vue';

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld,
    NavBar
  }
})
</script>

<style>
.nav-top {
  width: 100%;
  background: #242424;
}
.container {
  margin: 0 auto;
  width: 1100px;
}
</style>
