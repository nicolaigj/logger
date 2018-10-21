<template>
  <div class="home">
    <logger-input></logger-input>
  </div>
</template>

<script>
import LoggerInput from '@/components/LoggerInput.vue'

export default {
  name: 'home',
  components: {
    LoggerInput
  }
}
</script>

<style scoped>
.home {
  display: grid;
  grid-template-columns: 1fr minmax(200px, 500px) 1fr;
  grid-template-areas:
    "gutter-left content gutter-right";
  padding-top: 30px;
  grid-gap: 5px;
}
</style>
