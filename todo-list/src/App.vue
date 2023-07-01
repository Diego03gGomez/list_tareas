<script setup>

import lista from  './components/lista.vue';
</script>







<template>

  <div id="fondo">

    <header>
      <div class="cont_header">
        <h1>Tu Lista <img class="logo" src="../imagenes/logo.jpg" alt=""></h1> 
      </div>
    </header>

<div class="contenido">
  <div class="explicacion">
    <h1>Lista de tareas</h1>
<h4>Ingrese sus tareas en el input y agreguelas</h4>
  </div>


<lista></lista>

</div>


</div>
</template>

<style scoped>
.cont_header h1{
  display: flex;
  align-items: center;
}

.logo{
  border-radius: 10em;
  font-size: 9px;
}

.cont_header{
  margin: auto;
  width: 85%;
  font-size: 25px;
  color: white;
}

header{
  background-color: #080f28;
}

.contenido{
  background-color: #080f28a1;
 
 border-radius: 2em;
  margin:100px auto;
  width: 65%;
  text-align: center;
  border-color: #ffffff61;
    border-style: solid;
}
.explicacion{

 color: white;
 font-size: 30px;
}

@media (max-width:1024px){
  .contenido{
    width: 90%;
   
  
  }
}

@media(max-width:589px){
  .contenido{
    text-align: center;
  }
}




.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
