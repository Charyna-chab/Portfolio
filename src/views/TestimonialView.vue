<template>
    <!-- Testimonials Section -->
    <section class="py-20 bg-gray-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <span class="text-blue-400 font-semibold text-lg">Testimonials</span>
          <h2 class="text-5xl font-bold text-white mb-4">What Clients Say</h2>
          <p class="text-xl text-gray-300">Real feedback from amazing people I've worked with</p>
          <div class="w-24 h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto mt-6"></div>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div 
            v-for="(testimonial, index) in testimonials" 
            :key="testimonial.id"
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
            
            <div class="relative z-10">
              <!-- Quote Icon -->
              <div class="mb-6">
                <QuoteIcon :class="[
                  'w-10 h-10 opacity-50',
                  index % 3 === 0 ? 'text-blue-400' : '',
                  index % 3 === 1 ? 'text-purple-400' : '',
                  index % 3 === 2 ? 'text-green-400' : ''
                ]" />
              </div>
              
              <!-- Testimonial Text -->
              <p class="text-gray-200 text-lg leading-relaxed mb-6 italic group-hover:text-white transition-colors">
                "{{ testimonial.quote }}"
              </p>
              
              <!-- Rating -->
              <div class="flex mb-6">
                <StarIcon v-for="i in 5" :key="i" :class="[
                  'w-5 h-5 fill-current',
                  index % 3 === 0 ? 'text-blue-400' : '',
                  index % 3 === 1 ? 'text-purple-400' : '',
                  index % 3 === 2 ? 'text-green-400' : ''
                ]" />
              </div>
              
              <!-- Client Info -->
              <div class="flex items-center">
                <div class="relative">
                  <img :src="testimonial.avatar" :alt="testimonial.name" class="w-14 h-14 rounded-full border-2 border-white/20 group-hover:border-white/40 transition-colors">
                  <div :class="[
                    'absolute -inset-1 rounded-full opacity-0 group-hover:opacity-30 transition-opacity blur-sm',
                    index % 3 === 0 ? 'bg-blue-500' : '',
                    index % 3 === 1 ? 'bg-purple-500' : '',
                    index % 3 === 2 ? 'bg-green-500' : ''
                  ]"></div>
                </div>
                <div class="ml-4">
                  <h4 class="font-bold text-white text-lg group-hover:text-gray-100 transition-colors">{{ testimonial.name }}</h4>
                  <p :class="[
                    'text-sm font-medium',
                    index % 3 === 0 ? 'text-blue-300' : '',
                    index % 3 === 1 ? 'text-purple-300' : '',
                    index % 3 === 2 ? 'text-green-300' : ''
                  ]">{{ testimonial.role }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>
<script setup>
import { ref, computed } from 'vue'
import rady from '@/assets/image/rady.png'
import yon from '@/assets/image/yon.png'
import him from '@/assets/image/him.png'

// Testimonials data
const testimonials = ref([
  {
    id: 1,
    name: 'Rady Y',
    role: 'CEO, TechStart',
    quote: 'Charyna delivered an exceptional website that exceeded our expectations. Professional and reliable!',
    avatar: rady
  },
  {
    id: 2,
    name: 'Yon Yen',
    role: 'Marketing Director',
    quote: 'The mobile app Charyna developed for us has been a game-changer for our business.',
    avatar: yon
  },
  {
    id: 3,
    name: 'Him Hey',
    role: 'Startup Founder',
    quote: 'Charyna Service Amazing attention to detail and great communication throughout the project.',
    avatar: him
  }
])

</script>