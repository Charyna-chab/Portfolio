<template>
  <section class="py-6 bg-gray-900">
    <div class="max-w-5xl mx-auto px-4">
      <div class="text-center mb-4">
        <h2 class="text-xl font-bold text-white">Tools</h2>
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
</template>




<script setup>
import { ref } from 'vue'

const blogPosts = ref([
  {
    id: 1,
    title: 'Power BI',
    image: 'https://i.pinimg.com/736x/b8/87/63/b8876357eecb487ac780d266086bb55a.jpg'
  },
  {
    id: 2,
    title: 'Git',
    image: 'https://i.pinimg.com/736x/97/30/c7/9730c7b997bdc91dd083ff2a61383815.jpg'
  },
  {
    id: 3,
    title: 'Git Hub',
    image: 'https://i.pinimg.com/736x/4a/10/a1/4a10a1e719b4fc25cf4ed4ed59bf9e69.jpg'
  },
  {
    id: 4,
    title: 'AWS',
    image: 'https://i.pinimg.com/736x/09/3f/6e/093f6ed3ff0b96f50686bd538383ad9c.jpg'
  },
  {
    id: 5,
    title: 'Linux',
    image: 'https://i.pinimg.com/736x/c7/b8/11/c7b8113247fecd83bd9b5ed5bd3f34d5.jpg'
  },
  {
    id: 6,
    title: 'Canva',
    image: 'https://i.pinimg.com/736x/15/62/54/156254cda1120f9204f7a08238b81721.jpg'
  },
  {
    id: 7,
    title: 'Figma',
    image: 'https://i.pinimg.com/736x/5a/7a/09/5a7a09170e9273d6e60775d031daaf89.jpg'
  },
  {
    id: 8,
    title: 'Draw.io',
    image: 'https://i.pinimg.com/736x/d7/da/8f/d7da8fb8e63f41d120216256004ee99c.jpg'
  },
  {
    id: 9,
    title: 'LucidChat',
    image: 'https://i.pinimg.com/736x/8a/31/ea/8a31ea5cd91593170acfbd44cc6b8823.jpg'
  },
  {
    id: 10,
    title: 'Netlify',
    image: 'https://i.pinimg.com/736x/92/b5/e3/92b5e3dec20621f62aaafb0b7a2fd8c3.jpg'
  },
  {
    id: 11,
    title: 'Vercel',
    image: 'https://i.pinimg.com/736x/91/12/ae/9112ae1e604de6011eab619a1a5e96ec.jpg'
  },
  {
    id: 12,
    title: 'Postman',
    image: 'https://i.pinimg.com/736x/af/70/80/af70800826083538b7cfab54a98c55f1.jpg'
  },
  {
    id: 13,
    title: 'Jira',
    image: 'https://i.pinimg.com/736x/37/0a/6c/370a6cb7a084c4b4c2fe667147509e1b.jpg'
  },
])
</script>

