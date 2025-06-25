<template>
 <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-white/90 backdrop-blur-sm border-b border-gray-200 z-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex justify-between items-center py-4">
          <div class="text-2xl font-bold text-gray-900">Charyna</div>
          <div class="hidden md:flex space-x-8">
            <a href="#home" class="text-gray-700 hover:text-blue-600 transition-colors">Home</a>
            <a href="#about" class="text-gray-700 hover:text-blue-600 transition-colors">About</a>
            <a href="#projects" class="text-gray-700 hover:text-blue-600 transition-colors">Projects</a>
            <a href="#services" class="text-gray-700 hover:text-blue-600 transition-colors">Services</a>
            <a href="#contact" class="text-gray-700 hover:text-blue-600 transition-colors">Contact</a>
          </div>
          <button @click="toggleMobileMenu" class="md:hidden">
            <MenuIcon class="h-6 w-6" />
          </button>
        </div>
      </div>
      <!-- Mobile Menu -->
      <div v-if="mobileMenuOpen" class="md:hidden bg-white border-t border-gray-200">
        <div class="px-4 py-2 space-y-2">
          <a href="#home" class="block py-2 text-gray-700 hover:text-blue-600">Home</a>
          <a href="#about" class="block py-2 text-gray-700 hover:text-blue-600">About</a>
          <a href="#projects" class="block py-2 text-gray-700 hover:text-blue-600">Projects</a>
          <a href="#services" class="block py-2 text-gray-700 hover:text-blue-600">Services</a>
          <a href="#contact" class="block py-2 text-gray-700 hover:text-blue-600">Contact</a>
        </div>
      </div>
    </nav>
</template>

<script setup>
import { ref } from 'vue';

const navLinks = [
  { to: '#home', label: 'Home' },
  { to: '#about', label: 'About' },
  { to: '#portfolio', label: 'Portfolio' },
  { to: '#service', label: 'Services' },
  { to: '#testimonial', label: 'Testimonials' },
  { to: '#contact', label: 'Contacts' },
  { to: '#resume', label: 'Resumes' },
  { to: '#blog', label: 'Blog' }
];

const activeLink = ref('#home'); // default active

function setActive(id) {
  activeLink.value = id;

  const el = document.querySelector(id);
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' });
  }
}
</script>
