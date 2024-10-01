<script setup>
import { RouterLink } from 'vue-router';

defineProps({
  url: {
    type: String,
    required: false,
    default: '',
  },
  text: {
    type: String,
    required: true,
  },
  isDisabled: {
    type: Boolean,
    required: false,
    default: false,
  },
});
</script>

<template>
  <li class="list-none">
    <RouterLink
      class="block px-4 py-2 text-base"
      :class="{
        'text-gray-500 pointer-events-none opacity-50': isDisabled,
        'text-blue-500 hover:text-blue-600': !isDisabled
      }"
      activeClass="font-semibold text-blue-600"
      aria-current="page"
      :to="url"
      :aria-disabled="isDisabled"
    >
      {{ text }}
    </RouterLink>
  </li>
</template>