<template>
  <div
    className="movies" 
    v-for="movie in movies" 
    :key="movie.imdbID"
  >
    <Movie 
     :movie="movie"
    />
  </div>
</template>

<script>

  import axios from 'axios';
  import Movie from './Movie.vue'

  export default {
    name: "Movies",

    components:{
      Movie
    },

    data(){
      return{
        movies:[]
      }
    },

    created(){
      console.log('created')
       axios.get(`http://www.omdbapi.com/?s=spider&apikey=bdedf3e0`)
       .then(res=>{
         console.log(res.data.Search)
         this.movies = res.data.Search
         })
    }
    
  }
</script>


<style scoped>

.movies {
  margin-top: 50px;
}
</style>

