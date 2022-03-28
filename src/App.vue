<template>
  <div id="app">
    <header-disc :options="mapOptions"/>
    <main-disc @pass-data="dataMain"/>
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
  data () {
    return {
      characters: []
    }
  },
  computed: {
    mapOptions () {
      return this.characters.map(element => element.genre)
    }
  },
  methods: {
    dataMain (data) {
      this.characters = data
      console.log(data)
    }
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
