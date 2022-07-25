<template>
  <div>
    <fieldset>
      <legend>Ingrese una Ip Pública</legend>

      <input type="text" v-model="ip" />
      <button v-on:click="obtenerRespuesta">Consultar</button>
    </fieldset>
    <fieldset>
      <legend>Información de la Ip</legend>
      <ul>
        <li><b>Tipo de IP: </b>{{ tipodeIP }}</li>
        
        <hr>
        <li><b>Continente : </b>{{ continente }}</li>
        
        <hr>
        <li><b>País: </b>{{ pais }}</li>
       
        <hr>
        <li><b>Región:</b>{{ region }}</li>
        <hr>
        <li><b>Ciudad:</b>{{ ciudad }}</li>
        <hr>
        <li><b>Organización:</b> {{ organizacion }}</li>
        <hr>
        <li><b>Proveedor de Internet:</b>{{ proveedorDeInternet }}</li>
        <hr>
        <li><b>Bandera: </b><img v-if="imag" :src="imag" alt="no encontrado" /></li>
      </ul>
    </fieldset>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ip: null,
      tipodeIP: null,
      continente: null,

      pais: null,

      region: null,

      ciudad: null,

      organizacion: null,

      proveedorDeInternet: null,

      imag: null,
    };
  },
  computed: {
    async obtenerRespuesta() {
      const { type, continent, country, region, city, connection, flag } =
        await fetch( `https://ipwho.is/${this.ip}`).then((r) => r.json());
      var { img } = flag;
      var { org, isp } = connection;
      this.tipodeIP = type;
      this.continente = continent;
      this.pais = country;
      this.region = region;
      this.ciudad = city;
      this.organizacion = org;
      this.proveedorDeInternet = isp;
      this.imag = img;
    },
  },
};
</script>

<style>
</style>