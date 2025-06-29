<template>
  <!-- Footer -->
    <footer class="bg-black text-white py-12">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid md:grid-cols-3 gap-8">
          <div>
            <h3 class="text-2xl font-bold mb-4">Charyna</h3>
            <p class="text-gray-400">Web Developer based in Cambodia, creating beautiful digital experiences.</p>
          </div>
          <div>
            <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
            <div class="space-y-2">
              <a href="#home" class="block text-gray-400 hover:text-white transition-colors">Home</a>
              <a href="#about" class="block text-gray-400 hover:text-white transition-colors">About</a>
              <a href="#projects" class="block text-gray-400 hover:text-white transition-colors">Projects</a>
              <a href="#services" class="block text-gray-400 hover:text-white transition-colors">Services</a>
              <a href="#contact" class="block text-gray-400 hover:text-white transition-colors">Contact</a>
            </div>
          </div>
          <div>
            <h4 class="text-lg font-semibold mb-4">Connect</h4>
            <div class="flex space-x-4">
                <!-- LinkedIn -->
                <a
                  href="https://www.linkedin.com/in/charyna-chab-4b3b61344"
                  target="_blank"
                  class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors"
                >
                  <Linkedin class="w-5 h-5 text-white" />
                </a>

                <!-- Facebook -->
                <a
                  href="https://www.facebook.com/charyna.chab "
                  target="_blank"
                  class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors"
                >
                  <Facebook class="w-5 h-5 text-white" />
                </a>

                <!-- Telegram -->
                <a
                  href="https://t.me/chabcharyna"
                  target="_blank"
                  class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors"
                >
                  <Send class="w-5 h-5 text-white" />
                </a>
              </div>
          </div>
        </div>
        <div class="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
          <p>&copy; charyna student at PNC.</p>
        </div>
      </div>
    </footer>
</template>
<script setup>
import { Facebook, Linkedin, Send } from 'lucide-vue-next';
</script>
