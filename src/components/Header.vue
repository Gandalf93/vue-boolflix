<template>
  <div>
      <input 
        type="text"
        placeholder="Cerca"
        v-model= 'searchBar'
        @keyup="$emit('ricerca',searchBar)"
       />
      
  </div>
</template>

<script>

export default {
  name:'Header',
   data(){
     return{
         searchBar:''

     }
   }
}
</script>

<style lang='scss' scoped>

</style>