<template>
  <div id="app">
    <ComTexto etiquetaProp="Nombre" v-model="cliente.nombre"></ComTexto>
    <ComTexto etiquetaProp="Correo" v-model="cliente.correo"></ComTexto>
    <ComBoton @clickDesdeHijo="eventoApp"></ComBoton>
    <ComTabla :clientesProp="clientes"></ComTabla>
  </div>
</template>

<script>


const clienteObj={nombre:"john",correo:"correo@correo.com"};
const clienteArreglo=[];


import ComTexto from "@/components/ComTexto";
import ComBoton from "@/components/ComBoton";
import ComTabla from "@/components/ComTabla";
export default {
  name: 'App',
  data() {
    return {cliente:clienteObj,clientes:clienteArreglo};
    },
  methods:{
    eventoApp() {
      // crea un clon: Object.assign({},  this.cliente) (una copia de los datos)
      this.clientes.push(Object.assign({},  this.cliente) );
      this.cliente={nombre:"",correo:""};
    }
  }
  ,components: {
    ComTabla,
    ComBoton,
    ComTexto

  }
}
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
