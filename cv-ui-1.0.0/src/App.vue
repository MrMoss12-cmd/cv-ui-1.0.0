<script setup lang="ts">
import { RouterView } from 'vue-router';
import NavbarBootstrap from './components/NavbarBootstrap.vue';
import UseCard from './components/UseCard.vue';
</script>

<template>
  <div>
    <!-- Barra lateral fija -->
    <div class="sidebar" style="margin-left: 3rem; margin-top: 1.2rem;">
      <UseCard />
    </div>

    <!-- Menu Navbar fijo -->
    <div class="navbar fixed-top" style="margin-left: 2rem;" >
      <NavbarBootstrap />
    </div>
    
    <!-- Contenido principal desplazable -->
    <div class="main-content" style="margin-top: 14rem; margin-left: 21rem;">
      <transition name="fade">
        <RouterView />
      </transition>
    </div>
  </div>
</template>

<style scoped>
/* Barra Horizontal fija */
.navbar {
  margin-left:25rem;
  margin-top: 3rem;
  width: 56rem;

}

/* Barra lateral fija */
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  width: 300px;
  height: 100vh;
  padding: 1rem;
}

/* Espaciado del contenido principal */
.main-content {
  margin-left: 320px; /* Separación del sidebar */
  padding: 2rem;
}
</style>