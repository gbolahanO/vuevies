<template>
  <div class="container mt-3">
    <div class="row">
      <form action="" v-on:submit.prevent="searchmovies">
        <input type="text" v-model="movie">
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      movie: ''
    }
  },
  components: {
  },
  methods: {
    searchmovies: function() {
      
    }
  }
}
</script>

<style>

</style>

