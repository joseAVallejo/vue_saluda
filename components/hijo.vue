<template> 
    <h2>Encabezado H2 del componente Hijo</h2>
    <h1>Saludos {{ nombre }}</h1>
</template>
<script>

export default {
    name: "Saluda al nombre recibido",
    // Con el uso de props establecemos comunicación descendente
    props: {
        nombre: String,
        edad: Number,
    }

}
</script>

<style scoped>
h2 {
    color: orange;
}
</style>