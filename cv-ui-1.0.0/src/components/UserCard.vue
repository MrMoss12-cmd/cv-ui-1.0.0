<template>
  <div class="card shadow-sm">
    <!-- Card Image Top -->
    <img
      src="https://via.placeholder.com/150"
      class="card-img-top rounded-circle mx-auto mt-4"
      alt="User Image"
      style="width: 100px; height: 100px;"
    />

    <!-- Card Body -->
    <div class="card-body">
      <!-- Card title -->
      <h5 class="card-title fw-bold">{{ user.name }}</h5>
      <p class="text-muted">{{ user.job }}</p>

      <!-- List Group -->
      <ul class="list-group list-group-flush text-start">
        <li class="list-group-item">
          <strong>Name:</strong> {{ user.name }}
        </li>
        <li class="list-group-item">
          <strong>Birthday:</strong> {{ user.birthday }}
        </li>
        <li class="list-group-item">
          <strong>Job:</strong> {{ user.job }}
        </li>
        <li class="list-group-item">
          <strong>Email:</strong>
          <a href="mailto:{{ user.email }}" class="text-decoration-none">{{ user.email }}</a>
        </li>
      </ul>

      <!-- Botón  -->
      <button @click="downloadCv" class="btn btn-warning mt-3">
        Download CV <i class="bi bi-download"></i>
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
const user = {
  name: "Elias Higuera",
  birthday: "10 Novenber 1995",
  job: "Junior Developer",
  email: "eliashigueraacosta1@hotmail.com",
  gitHub: "MrMoss12-cmd"
};

function downloadcv() {
  //logica de descarga
  alert("Descargando cv...");   
}

</script>

<style scoped>

  /* Estilos generales de la tarjeta */ 
  .card {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 100%;
    height: auto;
    display: flex;
    border: 1px solid #e0e0e0;
    border-radius: 0.5rem;
    overflow: hidden;
    flex-direction: column;
    align-items: center;
    text-align: center;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    box-sizing: border-box;
    background-color:#fff;
  }

  /* */
  .card-img-top {
    display: block;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin: 1rem auto;
    object-fit: cover;
  }

  /* */
  .card-body {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    box-sizing: border-box;
    text-align: center;
  }

  .card-title {
    font-size: 1rem;
    font-weight: bold;
    margin-bottom: 0.2rem;
  }

  .list-group {
    width: 90%;
    margin: 1rem 0;
    padding: 0;
    list-style: none;
    margin-top: 0.1rem;
  }

  .list-group-item {
    display: flex;
    justify-content: space-between;
    padding: 0.5rem 0.8rem;
    border-bottom: 1px solid #e0e0e0;
    font-size: 0.7rem;
  }

  .list-group-item:last-child {
    border-bottom: none;
    
  }

  .btn {
    width: 80%;
    padding: 0.65rem;
    font-size: 1rem;
    border-radius: 0.5rem;
    color: #000;
    cursor: pointer;
    transition: background-color 0.3s;
  }

  .btn:hover {
    background-color: #e0a800;
  }

</style>