<script setup lang="ts">
import { RouterView } from 'vue-router';
import NavbarBootstrap from './components/NavbarBootstrap.vue';
import UserCard from './components/UserCard.vue';
</script>

<template>
  <!-- Vista Screen -->
  <div class="screen">
    <!-- Barra lateral fija -->
    <div class="sidebar" style="margin-left: 3rem; margin-top: 1.2rem;">
      <UserCard />
    </div>

    <!-- Vista Pagina -->
    <div class="main-page">
      <!-- Header de la pagina -->
      <div class="header" style="margin-left: 2rem;" >
        <NavbarBootstrap />
      </div>     
      <!-- Contenido principal de la pagina -->
      <div class="main-content" style="margin-top: 14rem; margin-left: 21rem;">
        <transition name="fade">
          <RouterView />
        </transition>
      </div>
      <!-- Footer de la pagina -->
      <div class="footer" style="margin-left: 2rem;" >
        <NavbarBootstrap />
      </div> 
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