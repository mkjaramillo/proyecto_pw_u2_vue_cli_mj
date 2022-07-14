<template>
<div>


  <h2> {{muestraTitulo}}</h2>
  <p>{{ numero }} <sup>2</sup>= {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup>= {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup>= {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup>= {{ obtenerCuadradoComputado }}</p>
  <p>{{ numero }} <sup>2</sup>= {{ obtenerCuadradoComputado }}</p>
  <div>
    <button v-on:click="incrementar" >+1</button>
    <button v-on:click="decrementar">-1</button>
  </div>
  </div>
</template>

<script>
export default {
  name: "Contador123",
  props:['titulo','inicio'],
  data() {
    return {
      numero: this.inicio,
    };
  },
  methods: {
    obtenerCuadrado() {
      console.log("entro al calculo ");
      return this.numero * this.numero;
    },
    incrementar(){
        return this.numero++
    },
    decrementar(){
        return this.numero--
    }
  },
  computed: {
    obtenerCuadradoComputado() {
      console.log("entro al calculo computado ");

      return this.numero * this.numero;
    },
    muestraTitulo(){
     return this.titulo||'Titulo vacio2'
    }
  },
};
</script>

<style scoped>
button{
    background-color: lightgreen;
    border-radius: 5px;
    color: white;
    margin: 0px 5px;
    cursor: pointer;
}
button:hover{
    background-color: #5aa67b;
    transition: 0.9s ease-in-out;
}
</style>
