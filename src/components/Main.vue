<template>
  <div class="container">
    <div class="cards">
      <h2>Stai cercando: {{searched}}</h2>
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
   searched: String,
 }
}
</script>

<style lang='scss' scoped>

</style>