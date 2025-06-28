<template>
   <!-- Projects Section -->
     <section id="projects" class="py-20 bg-gray-900">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-5xl font-bold text-white mb-4">My Projects</h2>
          <p class="text-xl text-gray-300">Showcasing my latest work and creative solutions</p>
          <div class="w-24 h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto mt-6"></div>
        </div>
        
        <!-- Project Filter -->
        <div class="flex flex-wrap justify-center gap-4 mb-12">
          <button 
            v-for="category in projectCategories" 
            :key="category"
            @click="selectedCategory = category"
            :class="[
              'px-8 py-3 rounded-full font-semibold transition-all duration-300 transform hover:scale-105',
              selectedCategory === category 
                ? 'bg-gradient-to-r from-blue-600 to-purple-600 text-white shadow-lg' 
                : 'bg-gray-800 text-gray-300 hover:bg-gray-700 border border-gray-700'
            ]"
          >
            {{ category }}
          </button>
        </div>

        <!-- Projects Grid -->
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div 
            v-for="project in projects" 
            :key="project.id"
            class="group bg-gray-800 rounded-2xl overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2 border border-gray-700 hover:border-blue-500/50"
          >
            <div class="relative overflow-hidden">
              <img :src="project.image" :alt="project.name" class="w-full h-48 object-cover group-hover:scale-110 transition-transform duration-500">
              <div class="absolute inset-0 bg-gradient-to-t from-gray-900/80 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              <div class="absolute top-4 right-4 opacity-0 group-hover:opacity-100 transition-opacity duration-300">
                <span class="bg-blue-600 text-white text-xs px-3 py-1 rounded-full font-semibold">{{ project.category }}</span>
              </div>
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold text-white mb-2 group-hover:text-blue-400 transition-colors">{{ project.name }}</h3>
              <p class="text-gray-300 mb-4 leading-relaxed">{{ project.description }}</p>
              <div class="flex flex-wrap gap-2 mb-6">
                <span 
                  v-for="tech in project.technologies" 
                  :key="tech"
                  class="text-xs bg-gray-700 text-gray-300 px-3 py-1 rounded-full border border-gray-600"
                >
                  {{ tech }}
                </span>
              </div>
              <div class="flex gap-4">
                <a :href="project.liveUrl" class="flex items-center text-blue-400 hover:text-blue-300 font-semibold transition-colors">
                  <ExternalLinkIcon class="w-4 h-4 mr-2" />
                  Live Demo
                </a>
                <a :href="project.githubUrl" class="flex items-center text-gray-400 hover:text-white font-semibold transition-colors">
                  <GithubIcon class="w-4 h-4 mr-2" />
                  Code
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>
<script setup>
import { ref, computed } from 'vue'
import brochureImage from '@/assets/image/Brochure.jpg'
import posSystemImage from '@/assets/image/pos-system.png'
import canImage from '@/assets/image/canteen.png'
import quizImage from '@/assets/image/quiz.png'
import autoImage from '@/assets/image/auto.png'
// Project categories
const projectCategories = ['All', 'Web Development', 'UI Design', 'Mobile App']

// Projects data
const projects = ref([
  {
    id: 1,
    name: 'POS System',
    category: 'Web Development',
    description: 'A full-stack e-commerce solution with payment integration',
    image: posSystemImage,
    technologies: ['HTML', 'PHP', 'MySQL', 'CSS'],
    liveUrl: '#',
    githubUrl: 'https://github.com/Charyna-chab/VC1-Group8-Drink'
  },
  {
    id: 2,
    name: 'Automate Generation Document',
    category: 'Web Development',
    description: 'Modern portfolio design for a creative agency',
    image: autoImage,
    technologies: ['Algorithm', 'Tinker'],
    liveUrl: '#',
    githubUrl: 'https://github.com/Soda-Morn/G10-automated-document-generation-transcript-certificates-'
  },
  {
    id: 3,
    name: 'Quiz App',
    category: 'Mobile App',
    description: 'Cross-platform mobile app for task management',
    image: quizImage,
    technologies: ['JavaScript', 'HTML', 'CSS','Bootstrap','API'],
    liveUrl: '#',
    githubUrl: 'https://github.com/Charyna-chab/JS-project-G13'
  },
  {
    id: 4,
    name: 'Canteen Website',
    category: 'UI Design',
    description: 'Responsive website for a local restaurant',
    image: canImage,
    technologies: ['HTML', 'CSS'],
    liveUrl: '#',
    githubUrl: 'https://github.com/Charyna-chab/canteen-pnc'
  },
  {
    id: 5,
    name: 'Brochure',
    category: 'UI Design',
    description: 'Complete brand identity design for a startup',
    image: brochureImage,
    technologies: ['Figma'],
    liveUrl: '#',
    githubUrl: '#'
  },
  
])

</script>