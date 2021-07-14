<template>
  <div class="container">
    <div class="cards">
      <Card v-for='movie in movies' :key='movie.id' :info='movie' />
    </div>
  </div>
</template>

<script>

import Card from "@/components/Card.vue";

export default {
 name : 'Main',
 components: {
   Card,
 },
 props:{
   movies: Array,
 }
}
</script>

<style lang='scss' scoped>

</style>