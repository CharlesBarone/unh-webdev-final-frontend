<template>
  <div class="container">
    <HeaderTop dealershipName="Cars R Us" authorName="Charles Barone" />

    <CarList :cars="cars" />

</div>
</template>

<script>

import HeaderTop from './components/HeaderTop.vue'
import CarList from './components/CarList.vue'

export default {
  name: 'App',
  components: {    
    HeaderTop,
    CarList
  },

  data(){
    return {
      cars: []
    }

  },

  methods: {

    // promises

      async fetchCars(){
          const res = await fetch('https://evening-beach-39077.herokuapp.com/api')
          const data = await res.json()
          console.log( data )
          return data
      }


  },
  async created(){
    this.cars = await this.fetchCars()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background-color: #F6F7EB;
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 50%;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}

</style>
