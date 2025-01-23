<template>
  <div class="card shadow-sm" style="width: 18rem; margin: auto; text-align: center; margin-top: 1rem;">
    <!-- Imagen del usuario -->
    <img
      src="https://via.placeholder.com/150"
      class="card-img-top rounded-circle mx-auto mt-4"
      alt="User Image"
      style="width: 100px; height: 100px;"
    />

    <div class="card-body">
      <!-- Nombre y profesión -->
      <h5 class="card-title fw-bold">{{ user.name }}</h5>
      <p class="text-muted">{{ user.job }}</p>

      <!-- Detalles -->
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
        <li class="list-group-item">
          <strong>Skype:</strong> {{ user.skype }}
        </li>
      </ul>

      <!-- Botón para descargar CV -->
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

.card-title {
  padding-bottom: 0.5rem;
}
.card-body {
  padding: 1rem 1.5rem;
}
.card{
  padding-top: 0rem;
  margin-top: 4rem;
}
</style>