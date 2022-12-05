<template>
    <div class="carlist">


        

        <div v-for="car in cars" :key="car.id" >
            <CarItem :car="car"/>
        </div>

    </div>
    


</template>'

<script>

    import CarItem from './CarItem.vue'


    export default{
        name: 'CarList',
        components: {
            CarItem
        },
        props:{
            
            cars: Array
        }
    }

</script>

<style scoped>

.carlist{

background-color: #F6F7EB;
padding: 1em;
color: gray;
}

</style>