<template>
<main>
    <div class="container">
        <div class="row">
            <div class="col d-lg-block d-md-none d-sm-none"></div>
            <div class="col-lg-2 col-md-4 col-sm-6 text-center mb-3" v-for="element in response" :key="element">
                <img class="img-fluid" :src="element.poster" :alt="element.author">
                <h3 class="text-uppercase">{{ element.title }}</h3>
                <div>{{ element.author }}</div>
                <div> {{ element.year }}</div>
            </div>
            <div class="col d-lg-block d-md-none d-sm-none"></div>
        </div>

        <div class="row">
            <div class="col d-lg-block d-md-none d-sm-none"></div>
            <div class="col-lg-2 col-md-4 col-sm-6 text-center mb-3" v-for="element in response" :key="element">
                <img class="img-fluid" :src="element.poster" :alt="element.author">
                <h3 class="text-uppercase">{{ element.title }}</h3>
                <div>{{ element.author }}</div>
                <div> {{ element.year }}</div>
            </div>
            <div class="col d-lg-block d-md-none d-sm-none"></div>
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
      success: true,
      response: null
    }
  },
  created () {
    axios.get(
      'https://flynn.boolean.careers/exercises/api/array/music')
      .then(function (ciao) {
        this.response = ciao.data.response
      })
  }
}

</script>
<style scoped lang='scss'>
main{
    background-color: rgb(30, 45, 59);
}

h3{
    color: white;
}

</style>
