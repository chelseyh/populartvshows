<template>
    
      <!-- <p v-for="show in showlist" v-bind:key="show.id">{{showlist.name}}</p> -->
            <!-- <h1>{{theTitle}}</h1> -->
            <!-- <p v-for="show in showlist" v-bind:key="show.id">{{show.name}}</p> -->
    <div class="row" >
      <div class="card col-3" >
        <img v-bind:src= "'https://image.tmdb.org/t/p/w500/' + showlist.poster_path " class="card-img-top" alt="...">
        <div  class="card-body">
          <h5 class="card-title">{{showlist.name}}</h5>
          <p class="card-text">{{show.overview}}</p>
          <a class="btn btn-dark">Button</a>
        </div>
      </div>
     </div>
  
</template>

<!--- below is where I'm exporting/importing data to be displayed from the component--->

<script>
// import Shows from './Shows.vue'
export default {
    name: 'ShowList',
    props: ['theTitle','showlist'],
    components:{
      // Shows
    },
//       data()
//   {
//     return{
//       showlist:''
//     }
// }
}
</script>