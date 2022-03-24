<template>
<main>
    <div class="container">
        <div class="row">
            <div class="col"></div>
            <div class="col-2" v-for="element in response" :key="element">
                <img class="img-fluid" :src="element.poster" :alt="element.author">
                <div>{{ element.author }}</div>
                <div> {{ element.year }}</div>
            </div>
            <div class="col"></div>
        </div>

        <div class="row">
            <div class="col"></div>
            <div class="col-2" v-for="element in response" :key="element">
                <img class="img-fluid" :src="element.poster" :alt="element.author">
                <div>{{ element.author }}</div>
                <div> {{ element.year }}</div>
            </div>
            <div class="col"></div>
        </div>
    </div>
</main>
</template>

<script>
/* import axios from 'axios' */
export default {
  name: 'MainDisc',
  data () {
    return {
      success: true,
      response: [
        {
          poster: 'https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg',
          title: 'New Jersey',
          author: 'Bon Jovi',
          genre: 'Rock',
          year: '1988'
        },
        {
          poster: 'https://img.discogs.com/vknPDdrqRbT92pNRX0W4I5N91jg=/fit-in/300x300/filters:strip_icc():format(jpeg):mode_rgb():quality(40)/discogs-images/R-1246953-1448927086-6590.jpeg.jpg',
          title: 'Live at Wembley 86',
          author: 'Queen',
          genre: 'Pop',
          year: '1992'
        },
        {
          poster: 'https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg',
          title: 'New Jersey',
          author: 'Bon Jovi',
          genre: 'Rock',
          year: '1988'
        },
        {
          poster: 'https://img.discogs.com/vknPDdrqRbT92pNRX0W4I5N91jg=/fit-in/300x300/filters:strip_icc():format(jpeg):mode_rgb():quality(40)/discogs-images/R-1246953-1448927086-6590.jpeg.jpg',
          title: 'Live at Wembley 86',
          author: 'Queen',
          genre: 'Pop',
          year: '1992'
        },
        {
          poster: 'https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg',
          title: 'New Jersey',
          author: 'Bon Jovi',
          genre: 'Rock',
          year: '1988'
        }
      ]
    }
  }
  /*
  created () {
    axios.get(
      'https://flynn.boolean.careers/exercises/api/array/music')
      .then(function (response) {
        /* this.boxes = response.data.response
        console.log(response.data.response)
      })
  } */
}
</script>

<style scoped lang='scss'>

</style>
