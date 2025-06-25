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
    excerpt: 'Learn the basics of Vue.js 3 and its new features',
    date: 'Dec 15, 2024',
    image: '/placeholder.svg?height=200&width=300'
  },
  {
    id: 2,
    title: 'Modern CSS Techniques',
    excerpt: 'Explore the latest CSS features and best practices',
    date: 'Dec 10, 2024',
    image: '/placeholder.svg?height=200&width=300'
  },
  {
    id: 3,
    title: 'Building Responsive Layouts',
    excerpt: 'Tips for creating layouts that work on all devices',
    date: 'Dec 5, 2024',
    image: '/placeholder.svg?height=200&width=300'
  }
])
</script>