<template>
  <section class="py-6 bg-gray-900">
    <div class="max-w-5xl mx-auto px-4">
      <div class="text-center mb-4">
        <span class="text-blue-400 text-sm font-semibold">Blog</span>
        <h2 class="text-xl font-bold text-white">Programming Languages</h2>
        <div class="w-12 h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto mt-2"></div>
      </div>

      <div class="grid grid-cols-3 sm:grid-cols-4 md:grid-cols-5 gap-4">
        <div
          v-for="post in blogPosts"
          :key="post.id"
          class="bg-white p-2 rounded-md shadow-sm flex items-center justify-center h-32"
        >
          <img
            :src="post.image"
            :alt="post.title"
            class="h-full w-auto object-contain"
          />
        </div>
      </div>
    </div>
  </section>
  <Tools/>
</template>




<script setup>
import Tools from '@/components/Blogs/Tools.vue';
import { ref } from 'vue'

const blogPosts = ref([
  {
    id: 1,
    title: 'Vue.js 3',
    image: 'https://i.pinimg.com/736x/de/ce/27/dece274f2547d597065ab1c189fd32af.jpg'
  },
  {
    id: 2,
    title: 'Laravel',
    image: 'https://i.pinimg.com/736x/38/bb/a9/38bba976a7268e24be31f1cc04408b06.jpg'
  },
  {
    id: 3,
    title: 'PHP',
    image: 'https://i.pinimg.com/736x/0f/77/4d/0f774d11c2f80008225f0f4181ec8e22.jpg'
  },
  {
    id: 4,
    title: 'HTML',
    image: 'https://i.pinimg.com/736x/fb/1e/7f/fb1e7f9db2540c3194a9179094a925e2.jpg'
  },
  {
    id: 5,
    title: 'CSS',
    image: 'https://i.pinimg.com/736x/8e/95/47/8e95479da2c5e493b835c8533c2d5ba5.jpg'
  },
  {
    id: 6,
    title: 'Python',
    image: 'https://i.pinimg.com/736x/ed/66/63/ed666327dd3ce274d94f2b3547155891.jpg'
  },
  {
    id: 7,
    title: 'Node.js',
    image: 'https://i.pinimg.com/736x/e3/a2/49/e3a2498d2fabe3948c98e784f7f51808.jpg'
  },
  {
    id: 8,
    title: 'JavaScript',
    image: 'https://i.pinimg.com/736x/49/9b/1d/499b1d8f955acd1d3ec30f217eddfa2a.jpg'
  },
  {
    id: 9,
    title: 'Bootstrap',
    image: 'https://i.pinimg.com/736x/c1/78/5d/c1785d50a929254419fa4aad0560b058.jpg'
  },
  {
    id: 10,
    title: 'MySql',
    image: 'https://i.pinimg.com/736x/09/7b/34/097b349ab1d78c15744c3a89ff457939.jpg'
  },
  {
    id: 11,
    title: 'Tailwind',
    image: 'https://i.pinimg.com/736x/14/74/9e/14749e54dbdf5a0acd58f67743a84afa.jpg'
  },
  {
    id: 12,
    title: 'SASS',
    image: 'https://i.pinimg.com/736x/eb/38/be/eb38be560364abb7ee39c5c4f4e05f7e.jpg'
  },
  {
    id: 13,
    title: 'OOP',
    image: 'https://i.pinimg.com/736x/a2/a4/9b/a2a49bee63c81d66c187d6ed94ee5528.jpg'
  },
])
</script>

