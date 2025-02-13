<template>
  <header class="header">
    <nav class="nav">
      <a href="#home" class="nav-link">
        <img src="/logo.png" alt="Logo" class="logo" />
      </a>
      <a href="#home" class="nav-link">Home</a>
      <a href="#projects" class="nav-link">Projects</a>
      <a href="#contact" class="nav-link">Contact</a>
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

<style>
html {
  scroll-behavior: smooth;
}

body {
  background-color: #2b2b2b;
  color: white;
  font-family: Arial, sans-serif;
}

.header {
  display: flex;
  justify-content: space-between;
  padding: 25px;
  background-color: #005f73;
  font-size: 1.25rem;
  font-weight: bold;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  align-items: center;
}

.logo {
  width: 75px;
  height: auto;
  padding-left: 10px;
  padding-right: 10px;
}

.nav {
  display: flex;
  gap: 22px;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
}

.nav-link {
  text-decoration: none;
  color: white;
  cursor: pointer;
}

.nav-link:hover {
  color: #ffdd57;
}

main {
  padding-top: 90px;
}
</style>
