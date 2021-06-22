<template>
  <tr>
    <td>{{filaProp.nombre}}</td>
    <td>{{filaProp.correo}}</td>
  </tr>
</template>

<script>
export default {
  name: "ComFila",
  props:["filaProp"]
}
</script>

<style scoped>

</style>