<template>
    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gray-900 text-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
          <h2 class="text-4xl font-bold mb-4">Get In Touch</h2>
          <p class="text-xl text-gray-300">Let's work together on your next project</p>
        </div>
        <div class="grid lg:grid-cols-2 gap-12">
          <!-- Contact Form -->
          <div>
            <form @submit.prevent="submitForm" class="space-y-6">
              <div>
                <label for="name" class="block text-sm font-medium mb-2">Name</label>
                <input 
                  v-model="form.name"
                  type="text" 
                  id="name" 
                  required
                  class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:outline-none focus:border-blue-500 text-white"
                >
              </div>
              <div>
                <label for="email" class="block text-sm font-medium mb-2">Email</label>
                <input 
                  v-model="form.email"
                  type="email" 
                  id="email" 
                  required
                  class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:outline-none focus:border-blue-500 text-white"
                >
              </div>
              <div>
                <label for="message" class="block text-sm font-medium mb-2">Message</label>
                <textarea 
                  v-model="form.message"
                  id="message" 
                  rows="5" 
                  required
                  class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:outline-none focus:border-blue-500 text-white"
                ></textarea>
              </div>
              <button 
                type="submit"
                class="w-full bg-blue-600 text-white px-8 py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors"
              >
                Send Message
              </button>
            </form>
          </div>
          
          <!-- Contact Info -->
          <div class="space-y-8">
            <div>
              <h3 class="text-2xl font-bold mb-6">Contact Information</h3>
              <div class="space-y-4">
                <div class="flex items-center">
                  <MailIcon class="w-6 h-6 text-blue-400 mr-4" />
                  <span>rady@example.com</span>
                </div>
                <div class="flex items-center">
                  <PhoneIcon class="w-6 h-6 text-blue-400 mr-4" />
                  <span>+855 12 345 678</span>
                </div>
                <div class="flex items-center">
                  <MapPinIcon class="w-6 h-6 text-blue-400 mr-4" />
                  <span>Phnom Penh, Cambodia</span>
                </div>
              </div>
            </div>
            
            <div>
              <h3 class="text-xl font-bold mb-4">Follow Me</h3>
              <div class="flex space-x-4">
                <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors">
                  <GithubIcon class="w-5 h-5" />
                </a>
                <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors">
                  <LinkedinIcon class="w-5 h-5" />
                </a>
                <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-blue-600 transition-colors">
                  <TwitterIcon class="w-5 h-5" />
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
// Computed properties
const mobileMenuOpen = ref(false)
const selectedCategory = ref('All')
const form = ref({
  name: '',
  email: '',
  message: ''
})
const filteredProjects = computed(() => {
  if (selectedCategory.value === 'All') {
    return projects.value
  }
  return projects.value.filter(project => project.category === selectedCategory.value)
})

// Methods
const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const submitForm = () => {
  // Handle form submission
  console.log('Form submitted:', form.value)
  alert('Thank you for your message! I\'ll get back to you soon.')
  form.value = { name: '', email: '', message: '' }
}
</script>