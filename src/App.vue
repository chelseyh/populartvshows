<template>
  <div id="app">
    <!-- <ShowList v-bind:showlist="displayshows"></ShowList> -->

    <!--this is where you are able to import the components into the page to display--->
    <Header pageheading="Popular TV Shows"/>
    <ShowList theTitle="My Shows" v-bind:showlist="displayshows"/>
  </div>
</template>

// <script>
// here is where I am importing my components and the ability to use bootstrap
import ShowList from './components/ShowList.vue'
import Header from './components/Header.vue'
import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.min.css'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    ShowList,
    Header
  },
  data()
  {
    return{
      displayshows:''
    }
  },

  //Below is my axios call to load in the tv shows from the API
  mounted()
  {
    axios.get('https://api.themoviedb.org/3/tv/popular?api_key=455b2956e19a9ac15cc1d8cc8831e2d8&language=en-US&page=1')
    .then( (response) =>
    {
      console.log(response.data)
      this.displayshows = response.data
    })
  }
}
</script>

