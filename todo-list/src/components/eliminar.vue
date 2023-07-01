<template lang="">
    <div>
        

<button @click="eliminar()" class="eliminar"><i class="fa-solid fa-trash"></i></button>


    </div>
</template>
<script>

export default {
    
methods: {
    eliminar() {
        
        event.target.parentNode.parentNode.parentNode.remove();

    }
},


}
</script>
<style scoped>
button{
    background-color: blueviolet;
    color: white;
    font-size: 30px;
    padding: 10px 20px;
    border-color: blueviolet;
    border-style: solid;
}
    
</style>