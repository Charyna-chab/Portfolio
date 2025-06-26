<template>
        <div class="flex justify-center gap-4 mb-6">
        <!-- GitHub -->
        <a href="https://github.com/Charyna-chab" target="_blank" rel="noopener" class="w-12 h-12 bg-gray-700 hover:bg-blue-600 rounded-full flex items-center justify-center shadow-md hover:shadow-lg transition-all duration-300 cursor-pointer group">
        <Github class="w-6 h-6 text-gray-300 group-hover:text-white transition-colors" />
        </a>
        
        <!-- LinkedIn -->
        <a href="https://linkedin.com/in/charyna-chab-4b3b61344" target="_blank" rel="noopener" class="w-12 h-12 bg-gray-700 hover:bg-blue-600 rounded-full flex items-center justify-center shadow-md hover:shadow-lg transition-all duration-300 cursor-pointer group">
        <Linkedin class="w-6 h-6 text-gray-300 group-hover:text-white transition-colors" />
        </a>

        <!-- Telegram (using Send icon as placeholder) -->
        <a href="https://t.me/chabcharyna" target="_blank" rel="noopener" class="w-12 h-12 bg-gray-700 hover:bg-blue-600 rounded-full flex items-center justify-center shadow-md hover:shadow-lg transition-all duration-300 cursor-pointer group">
        <Send class="w-6 h-6 text-gray-300 group-hover:text-white transition-colors" />
        </a>
    </div>
</template>
<script setup>
import { Github, Linkedin, Send } from 'lucide-vue-next';
</script>