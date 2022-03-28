<template>
  <div id="app">
    <header-disc :options="mapOptions"/>
    <main-disc @pass-data="cardsMain" :pass-genre='passGenre' />
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
      console.log(data)
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
