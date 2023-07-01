<template lang="">
    <div>
    <div class="div_input">
        <input  v-model="valor_input" type="text" placeholder= "Ingrese su tarea"> <label for=""><button ref="boton"  v-on:click="agregar()" class="agregar"><i class="fa-solid fa-plus"></i></button></label>
    </div>   



<div class="tareas"  >
<div  v-for="(e, index) in tareas" :key="index" class="tarea">
    <h1> {{e.nombre}}  </h1>
<eliminar></eliminar>
</div>
</div>




    </div>
</template>


<script>
import eliminar from './eliminar.vue';
export default {
    components: {
    eliminar,
},
data() {
    return {

        tareas: [/*
{nombre:"pepe", edad: 36},
{nombre:"caca", edad: 20},
{nombre:"jaja", edad: 12}*/
],



valor_input :"",



    }
},

methods: {
    agregar() {
if(this.valor_input == null){

this.$refs.boton.disabled = false;

}else{
    console.log(this.valor_input);
this.tareas.push({nombre: this.valor_input, edad: 0});
this.valor_input = "";
}



    }
},
created () {

},


    
}
</script>



<style scoped>

.div_input{
    background-color: #080f28;
    margin: auto;
    width: 70%;
    display: flex;
    align-items: center;
    justify-content: space-around;
    padding: 10px 0;
}

.agregar{
    background-color: blueviolet;
    border-color: blueviolet;
    color: white;
    font-weight: bold;
    border-style: solid;
    cursor: pointer;
    font-size: 30px;
padding: 0px 20px;
}

.div_input input{
    width: 80%;
    font-size: 20px;
    padding: 10px 0px;
}

.tarea{
    background-color: blueviolet;
    margin: 10px 0;
    padding: 10px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: white;
}


@media (max-width:1024px){
.div_input{
    width: 100%;
}

.div_input input{
    width: 60%;
}

}

    
</style>