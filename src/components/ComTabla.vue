<template>
  <table border="1">
    <tr>
      <th>Nombre</th>
      <th>Correo</th>
    </tr>
      <ComFila v-for="fila in clientesProp" :filaProp="fila" v-bind:key="fila.nombre"></ComFila>
  </table>
</template>

<script>
import ComFila from "@/components/ComFila";
export default {
  name: "ComTabla",
  props:["clientesProp"],
  components: {ComFila}
}
</script>

<style scoped>

</style>