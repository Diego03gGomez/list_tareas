<template lang="">
    <div>
    
    <div class="div_input">
        <input class="input" v-model="valor_input" type="text" placeholder= "Ingrese su tarea"> <label for=""><button :disabled="esInputVacio" ref="boton"  v-on:click="agregar()" class="agregar"><i class="fa-solid fa-plus"></i></button></label>
    </div>   



<div class="tareas"  >
<div  v-for="(e, index) in tareas" :key="index" class="tarea">
    <h1> {{e.nombre}}  </h1>
<div class="botones"  >

    <button v-on:click="eliminar_tarea(index)" class="eliminar"><i class="fa-solid fa-trash"></i></button>
    <button v-on:click="tachar($event)" class="lapiz "  ><i class="fa-solid fa-pencil  "></i></button>

</div>


</div>
</div>




    </div>
</template>


<script>

export default {
    components: {

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

    console.log(this.valor_input);
this.tareas.push({nombre: this.valor_input, edad: 0});
this.valor_input = "";

    },
    eliminar_tarea(index) {
      this.tareas.splice(index, 1)

    },



    tachar(event){
event.currentTarget.parentNode.parentNode.querySelector("h1").classList.toggle('tachar');
    }
},
created () {

},
computed: {
   esInputVacio() {
      return this.valor_input.trim() === "";
    }

    
   
},

mounted () {
 


    
},


    
}
</script>


















<style scoped>

.tachar{
    text-decoration: line-through;
}


.botones{
    display: flex;
    gap: 10px;
}
.lapiz{
    cursor: pointer;
    font-size: 30px;
    color: white;
    background-color: blueviolet;
    border-color: blueviolet;
    border-style: solid;
}


.div_input{
   
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
border-radius: 10px;
}

.div_input input{
    width: 80%;
    font-size: 20px;
    padding: 10px 0px;
    border-radius: 10px;
    border-color: white;
    border-style: solid;
}

.tarea{
    background-color: blueviolet;
    margin: 10px 0;
    padding: 10px 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    color: white;
    border-radius: 10px;
    width: 70%;
    margin: 10px auto;
}

.eliminar{
    background-color: blueviolet;
    border-color: blueviolet;
    border-style: solid;
    color: white;
    font-size: 30px;
cursor: pointer;
}



@media (max-width:1024px){
.div_input{
    width: 100%;
}

.div_input input{
    width: 81%;
}

}

    
</style>