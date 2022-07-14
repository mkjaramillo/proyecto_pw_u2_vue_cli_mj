<template>
<div>
  <img alt="Vue logo" src="./assets/logo.png" />

 <!-- <HelloWorld msg="Bienvenido" />-->
 <Contador2 titulo="Titulo 1"  v-bind:inicio="valorInicio"/>
 <Contador2 titulo="Titulo 2" v-bind:inicio="-1" />
<DatosBasicos v-bind:nombre="tipo" v-bind:apellido="tipo" v-bind:correo="tipo"/>
<DatosBasicos v-bind:nombre="tipo2" v-bind:apellido="tipo2" v-bind:correo="tipo2"/>
 
 <br>
 <div>
    <Calculadora></Calculadora>
 </div>
 
 </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Contador from"./components/Contador.vue";
import Calculadora from"./components/Calculadora.vue";
import Contador2 from "./components/Contador2.vue";
import DatosBasicos from"./components/DatosBasicos.vue"
export default {
  name: "App",
  data() {
    return {
      valorInicio:27,
      tipo:'Estudiante',
      tipo2:'Profesor'
    };
  },
  components: {
    Contador,
    Calculadora,
    Contador2,
    DatosBasicos
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
