<template>
<div>
<label for="">Nombre {{nombre}}:</label>
  <input type="text ">
  <label for="">Apellido {{apellido}}:</label>
  <input type="text">
  <label for="">Correo  {{correo}}:</label>
  <input type="text">
</div>
  
</template>

<script>
export default {
props:{
    correo:String,
    nombre:String,
    apellido:String,
    tipo:String
}
}
</script>

<style>
label{
    display: block;
}
</style>