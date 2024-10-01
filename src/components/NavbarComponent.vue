<script setup>
import NavLink from './NavLink.vue';
import { RouterLink } from 'vue-router';
import { ref } from 'vue';

const isMenuOpen = ref(false);
</script>

<template>
  <nav class="bg-gray-900 top-0 h-full z-50">
    <div class="container mx-auto flex-col h-full items-center">
      <ul class="flex flex-col items-center space-y-4 md:space-y-0 p-3">
      <RouterLink class="text-white text-lg font-bold" to="/">T</RouterLink>
      </ul>
      <button
        class="text-white md:hidden focus:outline-none"
        @click="isMenuOpen = !isMenuOpen"
        aria-controls="navbarCollapse"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <svg
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16m-7 6h7"
          ></path>
        </svg>
      </button>
      <div :class="{'block': isMenuOpen, 'hidden': !isMenuOpen}" class="w-full md:w-auto md:flex md:items-center">
        <ul class="flex flex-col items-center space-y-4 md:space-y-0">
          <NavLink url="/" text="H" />
          <NavLink url="/about" text="A" />
        </ul>
      </div>
    </div>
  </nav>
</template>