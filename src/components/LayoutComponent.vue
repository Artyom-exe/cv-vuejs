<script setup>
import Nav from '../components/NavbarComponent.vue';
import Footer from '../components/FooterComponent.vue';
</script>

<template>
  <div class="flex min-h-screen">
    <header>
      <Nav />
    </header>

    <div class="flex flex-col w-1/2 bg-gray-100">
      <div class="overflow-y-scroll p-4 flex-grow">
        <slot></slot>
        <p>Voici du contenu qui prend toute la hauteur et plus, ce qui permet d'activer la barre de défilement.</p>
      </div>
    </div>

    <div class="w-1/2 bg-[url('https://via.placeholder.com/800x1000')] bg-cover bg-center">
    </div>

    <Footer />
  </div>
</template>