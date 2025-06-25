<template>
    <!-- Blog Section -->
    <section class="py-20 bg-gray-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <span class="text-blue-400 font-semibold text-lg">Blog</span>
          <h2 class="text-5xl font-bold text-white mb-4">Latest Articles</h2>
          <p class="text-xl text-gray-300">Insights, tutorials, and thoughts from my development journey</p>
          <div class="w-24 h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto mt-6"></div>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-12">
          <article 
            v-for="post in blogPosts" 
            :key="post.id"
            class="group transition-all duration-300"
          >
            <!-- Image -->
            <div class="relative overflow-hidden rounded-xl mb-6">
              <img :src="post.image" :alt="post.title" class="w-full h-48 object-cover group-hover:scale-105 transition-transform duration-500 grayscale group-hover:grayscale-0">
              <div class="absolute inset-0 bg-black/20 group-hover:bg-black/40 transition-colors duration-300"></div>
            </div>
            
            <!-- Content -->
            <div>
              <div class="flex items-center gap-4 mb-3">
                <span class="text-blue-400 text-sm font-medium">{{ post.category }}</span>
                <span class="text-gray-500 text-sm">{{ post.date }}</span>
              </div>
              
              <h3 class="text-2xl font-bold text-white mb-3 group-hover:text-blue-400 transition-colors leading-tight">{{ post.title }}</h3>
              <p class="text-gray-400 mb-4 leading-relaxed">{{ post.excerpt }}</p>
              
              <div class="flex items-center justify-between pt-4 border-t border-gray-800">
                <span class="text-gray-500 text-sm">{{ post.readTime }} min read</span>
                <a href="#" class="text-blue-400 hover:text-blue-300 font-semibold transition-colors">
                  Read Article →
                </a>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>
</template>
<script setup>
import { ref, computed } from 'vue'
// Blog posts data
const blogPosts = ref([
  {
    id: 1,
    title: 'Getting Started with Vue.js 3',
    excerpt: 'Vue is popular for its simplicity and smooth integration with existing projects and offers reactive data binding.',
    date: 'Jun 25, 2025',
    image: 'https://i.pinimg.com/736x/de/ce/27/dece274f2547d597065ab1c189fd32af.jpg'
  },
  {
    id: 2,
    title: 'Laravel Framework',
    excerpt: 'Laravel is known for its clean syntax, developer-friendly features, and robust ecosystem that speeds up development.',
    date: 'Jun 25, 2025',
    image: 'https://i.pinimg.com/736x/38/bb/a9/38bba976a7268e24be31f1cc04408b06.jpg'
  },
  {
    id: 3,
    title: 'PHP',
    excerpt: 'PHP works well with databases like MySQL and powers many content management systems, including WordPress.',
    date: 'Jun 25, 2025',
    image: 'https://i.pinimg.com/736x/0f/77/4d/0f774d11c2f80008225f0f4181ec8e22.jpg'
  }
])
</script>