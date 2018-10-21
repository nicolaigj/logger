<template>
  <div id="app">
    <loggerMenu></loggerMenu>
    <router-view class="component"/>
  </div>
</template>

<script>
import LoggerMenu from '@/components/LoggerMenu.vue'
export default {
  components: {
    LoggerMenu
  }
}
</script>

<style>
:root {
  --orange: #FF9756;
  --grey: #525252;
  --blue: #56ABFF;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #525252;
  display: grid;
  grid-template-columns: 1fr minmax(300px, 1000px) 1fr;
  grid-template-areas: "left-gutter content right-gutter";
}

.component {
  grid-area: content;
  grid-row: 2;
}
</style>
