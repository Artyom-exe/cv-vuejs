<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <div class="bg-gray-100 py-12">
    <div class="container mx-auto text-center">
      <h1 class="text-4xl font-bold mb-4">Bienvenue sur Mon Site Web</h1>
      <p class="text-lg mb-6">
        Votre source fiable d'informations et de ressources en ligne.
      </p>
      <RouterLink
        to="/about"
        class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-3 px-6 rounded-lg"
      >
        En savoir plus sur nous
      </RouterLink>
    </div>
  </div>
</template>