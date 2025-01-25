<template>
    <!-- Navbar -->
    <nav class="navbar">
  <!-- Ícono de inicio -->
  <div class="home-icon">
    <i class="bi bi-house"></i>
  </div>

  <!-- Enlaces del menú -->
  <ul class="navbar-nav">
    <li v-for="link in links" :key="link.name" class="nav-item">
      <a class="nav-link" :href="link.href">{{ link.name }}</a>
    </li>
  </ul>

  <!-- Íconos sociales -->
  <div class="social-links">
    <a v-for="social in socialLinks" :key="social.icon" :href="social.href" target="_blank">
      <i :class="`bi ${social.icon}`"></i>
    </a>
  </div>

  <!-- Botón "Hire Me" -->
  <button class="btn-hire">
    Hire Me <i class="bi bi-telegram"></i>
  </button>
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
    display:flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 2rem;
    background-color: #f8f9fa;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
  }

  .navbar .home-icon {
    display: flex;
    gap: 1.3rem;
    list-style: none;
  }

  .navbar .navbar-nav {
    display: flex;
    flex-direction: row;
    gap: 1.5rem;
    list-style: none;
    margin: 0;
    padding: 0;
    align-items: center;
  }
    
  .navbar .navbar-nav .nav-item {
    margin: 0;
  }

  .navbar .navbar-nav .nav-link {
    text-decoration: none;
    color:#333;
    font-weight: 600;
    font-size: 1rem;
    transition: color 0.3s ease;
  }

  .navbar .navbar-nav .nav-link:hover {
    color: #007bff;
  }

  .navbar .social-links {
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .navbar .social-links a {
    color: #333;
    font-size: 1.5rem;
    transition: color 0.3s ease;
  }

  .navbar .social-links a:hover {
    color :#007bff;
  }

  .navbar .btn-hire {
    background-color: #ffc107;
    border: none;
    color: #fff;
    padding: 0.5rem 1.5rem;
    font-size: 0.9rem;
    font-weight: bold;
    border-radius: 20px;
    transition: background-color 0.3s ease;
  }

  .navbar .btn-hire:hover {
    background-color: #e0a800;
  }

  @media (max-width: 768px) {
    .navbar {
      flex-wrap: wrap;
      justify-content: center;
    }

    .navbar .home-icon,
    .navbar .navbar-nav,
    .navbar .social-links,
    .navbar .btn-hire {
      margin-bottom: 1rem;
    }

    .navbar .navbar-nav {
      justify-content: center;
    }

    .navbar .social-links {
      justify-content: center;
    }
  }
  </style>
  