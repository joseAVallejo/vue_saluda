<template>
<div>
  <h2>Encabezado H2 del componente Padre</h2>
  <h3>Cual es tu nombre?</h3>
  <input type="text" v-model="nombre" placeholder="tu nombre" required>
  <button @click="cambiarNombre(nombre)">Saluda!</button>
  
  <!-- Enviamos al componente hijo el parametro -->
  <!-- Al cargar el componente enviamos el parametro de forma dinámica al componente hijo -->
  <Saludo v-if='mostrar' :nombre = "nombre" /> 
</div>  
</template>

<script>
// Este componente esta compuesto por otro que realiza el saludo
import Saludo from './hijo.vue'

export default {
  name: "Entrada nombre",
  components: {
    Saludo
  },
    data() {
      return {
        nombre: null,
        mostrar: false
      }
    },
    methods: {
      cambiarNombre(nombre) {
        this.nombre = nombre,
        this.mostrar = true,
        console.log(this.nombre)
      }
    }
}
</script>

<style scoped>
h2 {
  color: red;
}
</style>