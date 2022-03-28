<template>
<main>
    <div class="container py-5">
        <div class="row justify-content-center">
          <div class="col-lg-2 col-md-4 col-sm-6 text-center mb-3 py-3 card_dark m-3" v-for="element in characters" :key="element">
                <img class="img-fluid mb-3" :src="element.poster" :alt="element.author">
                <h3 class="text-uppercase mb-3">{{ element.title }}</h3>
                <div>{{ element.author }}</div>
                <div> {{ element.year }}</div>
            </div>
        </div>
    </div>
</main>
</template>

<script>
import axios from 'axios'
export default {
  name: 'MainDisc',
  data () {
    return {
      characters: null
    }
  },
  created () {
    axios.get(
      'https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
        this.characters = response.data.response
      })
  }
}

</script>
<style scoped lang='scss'>
main{
    background-color: rgb(30, 45, 59);
}

.card_dark{
  background-color: rgb(46, 58, 70);

  div{
    color: grey;
  }
}

h3{
    color: white;
}

</style>
