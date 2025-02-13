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
  padding: 20px;
  background-color: #005f73;
  font-size: 1.2rem;
  font-weight: bold;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  align-items: center;
}

.logo {
  width: 70px;
  height: auto;
  padding-left: 8px;
  padding-right: 8px;
}

.nav {
  display: flex;
  gap: 18px;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
}

.nav-link {
  text-decoration: none;
  color: white;
  cursor: pointer;
  font-size: 1.2rem;
  transition: font-size 0.3s ease;
}

@media (max-width: 768px) {
  .header {
    padding: 15px;
    font-size: 1rem;
  }

  .logo {
    width: 55px;
  }

  .nav {
    gap: 12px;
  }

  .nav-link {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .header {
    padding: 10px;
    font-size: 0.9rem;
  }

  .logo {
    width: 45px;
  }

  .nav {
    gap: 8px;
  }

  .nav-link {
    font-size: 0.9rem;
  }
}

main {
  padding-top: 80px;
}
</style>
