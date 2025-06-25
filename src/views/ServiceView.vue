<template>
    <!-- Services Section -->
    <section id="services" class="py-20 bg-gray-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <span class="text-blue-400 font-semibold text-lg">What I Offer</span>
          <h2 class="text-5xl font-bold text-white mb-4">My Services</h2>
          <p class="text-xl text-gray-300">Professional solutions tailored to your needs</p>
          <div class="w-24 h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto mt-6"></div>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div 
            v-for="(service, index) in services" 
            :key="service.id"
            :class="[
              'group relative p-8 rounded-2xl transition-all duration-500 transform hover:-translate-y-2 hover:shadow-2xl border',
              index % 3 === 0 ? 'bg-gradient-to-br from-blue-900 to-blue-800 border-blue-700 hover:border-blue-500' : '',
              index % 3 === 1 ? 'bg-gradient-to-br from-purple-900 to-purple-800 border-purple-700 hover:border-purple-500' : '',
              index % 3 === 2 ? 'bg-gradient-to-br from-green-900 to-green-800 border-green-700 hover:border-green-500' : ''
            ]"
          >
            <!-- Glow effect -->
            <div :class="[
              'absolute inset-0 rounded-2xl opacity-0 group-hover:opacity-20 transition-opacity duration-500 blur-xl',
              index % 3 === 0 ? 'bg-blue-500' : '',
              index % 3 === 1 ? 'bg-purple-500' : '',
              index % 3 === 2 ? 'bg-green-500' : ''
            ]"></div>
            
            <div class="relative z-10 text-center">
              <div :class="[
                'w-20 h-20 rounded-2xl flex items-center justify-center mx-auto mb-6 transition-all duration-300 group-hover:scale-110',
                index % 3 === 0 ? 'bg-blue-600 group-hover:bg-blue-500' : '',
                index % 3 === 1 ? 'bg-purple-600 group-hover:bg-purple-500' : '',
                index % 3 === 2 ? 'bg-green-600 group-hover:bg-green-500' : ''
              ]">
                <component :is="service.icon" class="w-10 h-10 text-white" />
              </div>
              <h3 class="text-2xl font-bold text-white mb-4 group-hover:text-gray-100 transition-colors">{{ service.name }}</h3>
              <p class="text-gray-300 mb-6 leading-relaxed group-hover:text-gray-200 transition-colors">{{ service.description }}</p>
              <div :class="[
                'text-3xl font-bold mb-4',
                index % 3 === 0 ? 'text-blue-400' : '',
                index % 3 === 1 ? 'text-purple-400' : '',
                index % 3 === 2 ? 'text-green-400' : ''
              ]">{{ service.price }}</div>
              <button :class="[
                'w-full py-3 px-6 rounded-lg font-semibold transition-all duration-300 transform group-hover:scale-105',
                index % 3 === 0 ? 'bg-blue-600 hover:bg-blue-500 text-white' : '',
                index % 3 === 1 ? 'bg-purple-600 hover:bg-purple-500 text-white' : '',
                index % 3 === 2 ? 'bg-green-600 hover:bg-green-500 text-white' : ''
              ]">
                Get Started
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>
<script setup>
import { ref, computed } from 'vue'

// Services data
const services = ref([
  {
    id: 1,
    name: 'Web Development',
    description: 'Custom websites and web applications built with modern technologies',
    price: 'From $500',
  },
  {
    id: 2,
    name: 'UI/UX Design',
    description: 'Beautiful and intuitive user interface and experience design',
    price: 'From $300',
  },
  {
    id: 3,
    name: 'Mobile Development',
    description: 'Cross-platform mobile applications for iOS and Android',
    price: 'From $800',
  }
])
</script>