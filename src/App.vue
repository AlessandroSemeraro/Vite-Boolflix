<script>
import AppSearch from './components/AppSearch.vue';
import AppMain from './components/AppMain.vue';
import axios from 'axios';

export default {
  data() {
    return {
      moviesList: [],
    }
  },
  methods: {
    getMovies(searchContent) {
      console.log(searchContent);

      axios.get('https://api.themoviedb.org/3/search/movie?api_key=c02b0fa7e683cfdd872a24f0a6ffeccf&query=' + searchContent)
        .then((response) => {
          // handle success
          
          this.moviesList=response.data.results
        })
        .catch(function (error) {
          // handle error
          console.log(error);
        });
    }
  },
 
  components: {
    AppSearch,
    AppMain
  }
}

</script>

<template>
  <AppSearch @search="getMovies" />
  <AppMain :movies="moviesList" />
</template>
  
<style lang="scss"></style>
