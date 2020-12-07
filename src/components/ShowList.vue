<template>
      <div class="card col-3">
        <img v-bind:src= "'https://image.tmdb.org/t/p/w200/' + eachshow.poster_path " class="card-img-top" alt="...">
        <div  class="card-body">
          <h5 class="card-title">{{eachshow.name}}</h5>
          <p class="card-text">{{eachshow.overview}}</p>
        </div>
        </div>

</template>

<!--- below is where I'm exporting/importing data to be displayed from the component--->

<script>
// import Shows from './Shows.vue'
export default {
    name: 'ShowList',
    props: ['theTitle','eachshow'],
    components:{
      // Shows
    },
}
</script>

<style scoped>

.card {
  padding: 5px;
  margin-top: 20px;
}

</style>