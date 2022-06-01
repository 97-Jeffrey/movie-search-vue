<template>
    <div className="movie">
        <img v-bind:src="movie.Poster" alt="">
        <div className="movie-info-class">
            <div className="movie-title">{{movie.Title}}</div>
            <div className="movie-year">Released In {{movie.Year}}</div>
            <div className="movie-type">Type: {{movie.Type}}</div> 
        </div>
    </div>
</template>



<script>

export default {
  name: 'movie',
  props:['movie']
}
</script>


<style scoped>


   
.movie {
  flex-grow: 2;
  display: flex;
  color: #fefefe;
  margin-bottom: 1rem;
}


.movie-info-class {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  padding-left: 1rem;
  border-top-right-radius: 0.5rem;
  border-bottom-right-radius: 0.5rem;
  background: #201f2f;
  overflow: hidden;
}

.movie-info-class:hover {
  background: rgba(207, 13, 65, 0.4);
}

.movie-title {
  font-weight: 700;
  font-size: 50px;
  margin-bottom: 20px;
}


.movie-year {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 10px;
}
.movie-type {
  font-weight: 700;
  font-size: 1.25rem;
}

</style>
