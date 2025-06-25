<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import HomeView from './views/HomeView.vue'
import AboutView from './views/AboutView.vue'
import ProjectView from './views/ProjectView.vue'
import ServiceView from './views/ServiceView.vue'
import TestimonialView from './views/TestimonialView.vue'
import BlogView from './views/BlogView.vue'
import ContactView from './views/ContactView.vue'
</script>

<template>
  <header>
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

    <div class="wrapper">
      <Navbar />
     
    </div>
  </header>
   <main>
    <section id="home">
      <HomeView />
    </section>
    <div class="w-full h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto"></div>
    <section id="about">
      <AboutView />
    </section>
    <div class="w-full h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto"></div>

    <section>
      <ProjectView/>
    </section>
    <div class="w-full h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto"></div>

    <section>
      <ServiceView/>
    </section>
    <TestimonialView/>
    <div class="w-full h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto"></div>
    <section>
      <BlogView/>
    </section>
    <div class="w-full h-1 bg-gradient-to-r from-blue-500 to-purple-500 mx-auto"></div>

    <section>
      <ContactView/>
    </section>
  </main>

  <!-- <RouterView /> -->
  <footer>
    <Footer/>
  </footer>
</template>

