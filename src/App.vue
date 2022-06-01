<template>
  <Header />
  <Movies />
</template>

<script>
  import Header from './components/Header.vue'
  import Movies from './components/Movies.vue'

  export default {
    name: "App",
    components: {
      Header,
      Movies
    }
  }
</script>

<style >
*{
  margin:0
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  background-color: #2c3e50;
  width:100%;
  min-height: 100vh;
  margin:0;
  

}
</style>
