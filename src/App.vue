<template>
  <div id="app">
    <header-disc :options="mapOptions" @selected-genre="passGenre"/>
    <main-disc @pass-data="cardsMain" :search="searchGenre" />
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
      characters: [],
      searchGenre: ''
    }
  },
  computed: {
    mapOptions () {
      return [...new Set(this.characters.map(element => element.genre))]
    }
  },
  methods: {
    cardsMain (data) {
      this.characters = data
    },
    passGenre (genre) {
      this.searchGenre = genre
    }
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
