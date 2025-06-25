<template>
    <div class="space-y-8">
    <div
      v-for="(exp, index) in experiences"
      :key="index"
      class="relative pl-8"
      :class="exp.highlight ? 'border-l-2 border-blue-500/30' : ''"
    >
      <div
        class="absolute -left-2 top-0 w-4 h-4 rounded-full shadow-lg"
        :class="exp.highlight ? 'bg-blue-500' : 'bg-gray-500'"
      ></div>
      <div
        class="p-6 rounded-lg shadow-xl transition-all duration-300"
        :class="exp.highlight
          ? 'bg-gray-800 border border-gray-700 hover:shadow-2xl hover:border-blue-500/50'
          : 'bg-gray-800/50 border border-gray-600'"
      >
        <span
          class="text-sm font-semibold px-3 py-1 rounded-full"
          :class="exp.highlight
            ? 'text-blue-400 bg-blue-500/10'
            : 'text-gray-400 bg-gray-600/20'"
        >
          {{ exp.year }}
        </span>
        <h4
          class="text-xl font-bold mt-3 mb-2"
          :class="exp.highlight ? 'text-white' : 'text-gray-200'"
        >
          {{ exp.title }}
        </h4>
        <p
          class="leading-relaxed"
          :class="exp.highlight ? 'text-gray-300' : 'text-gray-400'"
        >
          {{ exp.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const experiences = ref([
  {
    year: '2024 - Present',
    title: 'Passerelles Numeriqeus Cambodia',
    description: 'I am studying as a Web Development student.Who have both skills on Back-end and Front-end.',
    highlight: true
  },
  {
    year: '2020 - 2023',
    title: 'Hight School',
    description: 'Studied at Hun Sen Hight school. Focus on Science class and have BacII',
    highlight: true
  },
  {
    year: '2017 - 2020',
    title: 'Secondary School',
    description: 'Studied at Som Dach Ouv Me Secondary school.Focus on general subject and had exam for secondary school',
    highlight: true
  },
  {
    year: '2011 - 2016',
    title: 'Primary School',
    description: 'Studied at Veal Primary school.',
    highlight: true
  }
])
</script>