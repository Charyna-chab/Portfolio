<script setup lang="ts">
import SocailMedia from '@/components/About/SocailMedia.vue';
import TimeLine from '@/components/About/TimeLine.vue';

</script>

<template>
   <section class="py-20 bg-gray-900 text-white">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold text-white mb-4">My Story</h2>
        <p class="text-xl text-gray-300 max-w-3xl mx-auto">
          From curious beginner to passionate developer - here's my journey in tech
        </p>
      </div>
      
      <div class="grid lg:grid-cols-2 gap-16 items-start">
        <!-- Profile Section -->
        <div class="sticky top-8">
          <div class="bg-gradient-to-br from-gray-800 to-gray-700 rounded-3xl p-8 text-center border border-gray-600 shadow-2xl">
            <div class="relative mb-6">
              <!-- Glowing effect behind image -->
              <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-purple-600 rounded-full blur-2xl opacity-30 scale-110"></div>
              <img src="../assets/image/ryna.png" alt="Charyna" class="relative z-10 w-48 h-48 rounded-full mx-auto border-4 border-blue-500 shadow-xl object-cover">
            </div>
            <h3 class="text-2xl font-bold text-white mb-2">Charyna Chab</h3>
            <p class="text-blue-400 font-semibold mb-4">Web Developer</p>
            <p class="text-gray-300 mb-6 leading-relaxed">
              Passionate about creating digital solutions that make a real impact in people's lives.
            </p>
            
            <!-- Social Icons -->
            <SocailMedia/>
            
            <!-- Download Button -->
                <a
                  href="/charyna-cv.pdf"         
                  download                 
                  class="bg-gradient-to-r from-blue-600 to-purple-600 hover:from-blue-700 hover:to-purple-700 text-white px-8 py-3 rounded-full font-semibold transition-all duration-300 w-full shadow-lg hover:shadow-xl transform hover:scale-105 inline-block text-center"
                >
                  <DownloadIcon class="w-5 h-5 inline mr-2" />
                  Download Resume
                </a>

          </div>
        </div>
        <!-- Timeline -->
        <TimeLine/>
      </div>
    </div>
  </section>

</template>

