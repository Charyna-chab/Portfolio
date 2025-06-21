<template>
  <nav class="bg-gray-800 text-white p-4 flex items-center justify-between">
    <div class="flex space-x-4">
      <RouterLink
        v-for="link in navLinks"
        :key="link.to"
        :to="link.to"
        :class="[
          'rounded-md px-3 py-2 text-sm font-medium hover:bg-gray-700 hover:text-white',
          route.path === link.to ? 'bg-gray-600 text-white' : 'text-gray-300'
        ]"
      >
        {{ link.label }}
        </RouterLink>
    </div>
  </nav>
</template>
<script setup>
import { useRoute } from 'vue-router';

const route = useRoute();

const navLinks = [
  { to: '/', label: 'Home' },
  { to: '/about', label: 'About' },
  { to: '/portfolio', label: 'Portfolio' },
  { to: '/service', label: 'Services' },
  { to: '/testimonial', label: 'Testimonials' },
  { to: '/contact', label: 'Contacts' },
  { to: '/resume', label: 'Resumes' },
  { to: '/blog', label: 'Blog' }
];
</script>

