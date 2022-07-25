<template>
<div>
<ip-publica-vue></ip-publica-vue>
 </div>
</template>

<script>
import Pregunta from "./components/Pregunta.vue"
import IpPublicaVue from "./components/IpPublica.vue";
export default {
  name: "App",
  
  components: {
   Pregunta,
   IpPublicaVue
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
