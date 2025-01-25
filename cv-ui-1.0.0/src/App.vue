<script setup lang="ts">
import { RouterView } from 'vue-router';
import NavbarBootstrap from '@/components/NavbarBootstrap.vue';
import UserCard from '@/components/UserCard.vue';
import HeaderBootstrap from '@/components/HeaderBootstrap.vue';
</script>

<template>
  <!-- Vista Screen -->
  <div class="screen">
    <!-- Card lateral fija -->
    <div class="sidebar">
      <UserCard />
    </div>

    <!-- Vista Pagina -->
    <div class="main-page">
      <!-- Header de la pagina -->
      <HeaderBootstrap>
        <template #navbar>
          <NavbarBootstrap />
        </template>
      </HeaderBootstrap>  
      <!-- Contenido principal de la pagina -->
      <div class="main-content" >
        <transition name="fade">
          <RouterView />
        </transition>
      </div>
      <!-- Footer de la pagina -->
      <div class="footer" >
        <NavbarBootstrap />
      </div> 
    </div>
  </div>
</template>

<style scoped>
  /* configuracion general de screen*/
  .screen {
    display:flex; /* columnas */
    height: 100vh;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  /* Tarjeta lateral fija */
  .sidebar {
    width: 33%;
    max-width: 100%;
    height: 31rem;
    background-color: #f8f9fa;
    padding: 1rem;
    box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1) ;
    box-sizing: border-box;
    margin-left: 0.5rem;
    margin-top: 2.1rem;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: column;
    justify-content: flex-start;
    transition: width 0.3s, height 0.3s;
  }

  /*Contenedor principal */
  .main-page {
    flex: 1; /* ocupa el resto de espacio disponible*/
    display: flex;
    flex-direction: column;
    background-color: #ffffff;
    box-sizing: border-box;
  }

  /*Header */
  .header {
    background-color: #ffffff;
    padding: 1rem;
    box-sizing: border-box;
    margin-left: 5rem;
  }

  /*contenedor principal */
  .main-content {
    flex: 1; /*ocupa todo el espacio restante */
    padding: 1rem;
    text-align: center;
    box-sizing: border-box;
  }
</style>