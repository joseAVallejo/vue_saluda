<template>
  <!-- Cargamos el componente que solicita el nombre -->
  <Nombre/>
  
</template>

<script>
// Importamos el componente
import Nombre from './components/padre.vue';

export default {
  name: 'App',
  components: {
    Nombre
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
h1 {
  font-style: italic;
  color: #000;
}
h2 {
  color: green;
}
h3 {
  text-decoration: underline;
}
input {
  font-size: 20pt;
}
</style>
