<template>
  <header class="d-flex justify-content-between">
      <div><i class="fa-brands fa-spotify p-2 px-3 "></i></div>
      <select class="mx-3 my-2 rounded" name="genere" id="select">
        <option value="">All</option>
        <option v-for="element in options" :key="element" :value="element">{{ element }}</option>
      </select>
     </header>
</template>

<script>

export default {
  name: 'HeaderDisc',
  props: {
    options: Array
  },
  data () {
    return {
      selectValue: 'all'
    }
  }
}
</script>

<style scoped lang='scss'>
header{
    background-color: rgb(46, 58, 70);
}

i{
    color: rgb(26, 215, 96);
    font-size: 40px;
}

</style>
