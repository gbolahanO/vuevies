<template>
  <div>
    <div class="container mt-3">
      <div class="row">
        <div v-for="movie in movies" class="col-lg-3 col-md-4 col-sm-6 mt-2">
          <div class="card">
            <img class="card-img-top" :src=" 'https://image.tmdb.org/t/p/w300/' + movie.poster_path" :alt="movie.title">
            <div class="card-body">
              {{ movie.title }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data () {
    return {
      movies: [],
    }
  },
  created() {
    axios.get('https://api.themoviedb.org/3/discover/movie?api_key=087d8d1590b71f28a5472304c0cab8b9&language=en-US&sort_by=popularity.desc&include_adult=false&include_video=false&page=1')
    .then((response) => {
      console.log(response.data);
      this.movies = response.data.results;
    })
    .catch(errors => {
      console.log(errors);
    })
  }
}
</script>

<style>

</style>
