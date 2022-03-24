<template>
  <div id="app">
    <header-disc />
    <main-disc />
  </div>
</template>

<script>
import HeaderDisc from './components/HeaderDisc.vue'
import MainDisc from './components/MainDisc.vue'

export default {
  name: 'App',
  components: {
    HeaderDisc,
    MainDisc
  }
}
</script>

<style lang="scss">
</style>
