<template>
  <div class="container"> 
    <!-- <NavBar /> -->
    <div class="w-100 d-flex main-content">
       <CardsComponent />
    </div>
   
  </div>
</template>

<script>
import CardsComponent from './components/CardsComponent.vue'
/*import NavBar from './components/NavBar.vue'*/
export default {
  name: 'App',
  components: {
    CardsComponent,
    /*NavBar*/
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.container{
  width: 100%;
  max-width: 1200px;
  margin: 0px auto;
}
</style>
