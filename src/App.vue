<template>
  <div id="app">
    <Header @ricerca="ricercaFilm" />
    <Main :movies='arrayMovies' :searched='searchText' />
  </div>
</template>

<script>
import axios from 'axios';
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
  },

  data(){
    return{
    apiUrl : 'https://api.themoviedb.org/3/search/movie',
    apiKey : '397f04fd0d7d343757c0210631a38e24',
    language:'it-IT',
    arrayMovies: [],
    searchText:'',
    }
  },

  methods: {
    ricercaFilm(text){
      this.searchText= text;
      axios
          .get(this.apiUrl,{
            params:{
              api_key: this.apiKey,
              language: this.language,
              query: text,
            }
          })
          .then(response =>{
              // console.log(response.data.results);
              this.arrayMovies = response.data.results;
          });


      console.log(text);
    }
  },
};
</script>

<style lang="scss">
@import '@/assets/general.scss';
</style>
    
