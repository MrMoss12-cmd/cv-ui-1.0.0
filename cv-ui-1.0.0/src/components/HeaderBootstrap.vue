<template>
    <header class="header-bootstrap">
      <!-- Contenedor para el componente Navbar -->
      <slot name="navbar">
        <p>No Navbar provided!</p> <!-- Mensaje por defecto si no se pasa un slot -->
      </slot>
    </header>
</template>

<script>
export default {
    name: "HeaderBootstrap",
};
</script>

<style scoped>
.header-bootstrap {
  background-color: #f8f9fa; /* Fondo azul */
  color: #fff; /* Texto blanco */
  padding-left: 0rem; /* Espaciado interno */
  padding-top: 0rem;
  padding-bottom: 0rem;
  align-items: center;
  justify-content: center;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1); /* Sombra */
  box-sizing: border-box;
  margin-top: 2rem;
  margin-left: 2rem;
}
</style>