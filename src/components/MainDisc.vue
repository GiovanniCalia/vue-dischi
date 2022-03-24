<template>
<main></main>
</template>

<script>
export default {
  name: 'MainDisc',
  data () {
    return {
      axios: require('axios').get(
        'https://flynn.boolean.careers/exercises/api/array/music')
        .then(function (response) {
          console.log(response.data.response)
        })
    }
  }

}
</script>

<style scoped lang='scss'>

</style>
