<template>
  <header class="header">
    <nav class="navbar">
      <a href="#home" class="navbar-link">
        <img src="/logo.png" alt="Logo" class="navbar-logo" />
      </a>
      <a href="#home" class="navbar-link">Home</a>
      <a href="#projects" class="navbar-link">Projects</a>
      <a href="#contact" class="navbar-link">Contact</a>
    </nav>
  </header>

  <main>
    <Home />
    <Projects />
    <Contact />
  </main>
</template>

<script setup>
import Home from "./components/Home.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
</script>
