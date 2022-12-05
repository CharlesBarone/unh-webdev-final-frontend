<template>
    <div>
        <h1> {{dealershipName}} </h1>
        <h4> {{authorName}} </h4>
    </div>
</template>
    
    <script>
    
    export default{
        name: 'HeaderTop',
        props:{
            dealershipName: String,
            authorName:String
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
        text-align: center;
    }
    
    </style>