<template>
  <div id="app">
    <header-disc @seleziona="passSelezione"/>
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
  },
  methods: {
    passSelezione (data) {
      this.$emit('rilanciaSelezione', data)
    }
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
