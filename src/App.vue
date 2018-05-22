<template>
  <div>
    <app-navbar></app-navbar>
    <search-bar></search-bar>
    <movies></movies>
  </div>
</template>

<script>
import Navbar from './components/Navbar'
import SearchBar from './components/SearchBar'
import Movies from './components/Movies'
export default {
  data () {
    return {

    }
  },
  components: {
    'app-navbar': Navbar,
    'search-bar': SearchBar,
    'movies': Movies
  }
}
</script>

<style>

</style>

