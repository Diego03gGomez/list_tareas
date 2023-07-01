<script setup>

import lista from  './components/lista.vue';
</script>







<template>
<div class="contenido">
  <div class="explicacion">
    <h1>Lista de tareas</h1>
<h4>Ingrese sus tareas en el input y agreguelas</h4>
  </div>


<lista></lista>


  
  

</div>
</template>

<style scoped>

.contenido{
  background-color: #080f28;
  margin: auto;
  width: 45%;
  text-align: center;
}
.explicacion{
  background-color: #080f28;
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
