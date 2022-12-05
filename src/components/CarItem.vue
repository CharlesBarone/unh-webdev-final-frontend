<template>

    <div>
        <h2>{{car.year}} {{car.make}} </h2> - <h2> {{car.model}}</h2>
        <hr>
        <br>
        <h2>Color: </h2><h3>{{car.color}}</h3>
        <br>
        <h2>Description: </h2><h3>{{car.description}}</h3>
        <br>
        <h2>Price: </h2><h3>{{car.price}}</h3>
        <br>
        <h2>MPG: </h2><h3>{{car.mpg}}</h3>
        <br>
        <h2>Miles: </h2><h3>{{car.miles}}</h3>
        <br>
        <br>
        <h2>Availability: </h2>
        <div :class="car.availability ? 'green': 'red' " v-if="car.availability">Available</div>
        <div :class="car.availability ? 'green': 'red' " v-else-if="!car.availability">Unavailable</div>
    </div>

</template>

<script>


export default{
    name: 'CarItem',
    props:{
        car: Array
    }
}


</script>

<style scoped>

h2 {
    display: inline;
}

h3 {
    display: inline;
}


h4{
    margin: 2px;
    display: inline;
}

div{
    background-color: #88D498;
    color: black;
    padding: 1em;
}

.red{
    display: inline;
    background-color: orangered;
    height:2rem;
    width:6rem;
    text-align: center;
    line-height: 2rem;;
    font-size: 1rem;
    border-radius: 10%;
    color: white;
}

.green{
    display: inline;
    background-color: #1A936F;
    height:2rem;
    width:6rem;
    text-align: center;
    line-height: 2rem;;
    font-size: 1rem;
    border-radius: 10%;
    color: white;
}


</style>