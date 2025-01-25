<template>
    <nav class="navbar navbar-expand-lg bg-light shadow-sm " >
      <div class="container-fluid">
        <!-- Logo / Home Icon -->
        <a class="navbar-brand text-warning fw-bold" href="/">
          <i class="bi bi-house-fill"></i>
        </a>
  
        <!-- Botón de colapso para pantallas pequeñas -->
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
  
        <!-- Contenido del navbar -->
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li v-for="link in links" :key="link.name" class="nav-item">
              <a class="nav-link text-dark fw-semibold" :href="link.href">{{ link.name }}</a>
            </li>
          </ul>
  
          <!-- Redes sociales -->
          <div class="d-flex align-items-center">
            <a
              v-for="social in socialLinks"
              :key="social.icon"
              class="text-dark mx-2"
              :href="social.href"
              target="_blank"
              rel="noopener noreferrer"
            >
              <i :class="`bi ${social.icon} fs-5`"></i>
            </a>
          </div>
  
          <!-- Botón Hire Me -->
          <button class="btn btn-warning btn-sm ms-3">
            Hire Me <i class="bi bi-telegram"></i>
          </button>
        </div>
      </div>
    </nav>
  </template>
  
  <script setup>
  const links = [
    { name: "🏠", href: "/" },
    { name: "Resume", href: "/resume" },
    { name: "Portfolio", href: "/portfolio" },
    { name: "Blog", href: "/blog" },
    { name: "Contact", href: "/contact" },
  ];
  
  const socialLinks = [
    { icon: "bi-facebook", href: "https://facebook.com" },
    { icon: "bi-twitter", href: "https://twitter.com" },
    { icon: "bi-instagram", href: "https://instagram.com" },
    { icon: "bi-dribbble", href: "https://dribbble.com" },
  ];
  </script>
  
  <style scoped>


  /* Ajusta el contenido principal para evitar que quede oculto detrás del navbar */
  .navbar{
    margin-left: 0rem;
    margin-top: 0rem;
    padding:0;
    
  }


  .navbar-brand {
    font-size: 0.5rem;
  }

  .navbar-nav {
    font-size: 0.6rem;
  }
  
  /*Selector del elemento home */
  .navbar-nav li:first-child {
    background-color: yellow;
    margin-left: -2.1rem;
    width: 1.9rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  
  .btn {
    border-radius: 20px;
  }
  </style>
  