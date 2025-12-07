<script setup lang="ts">
// Import Vue composition API helpers
import { ref } from 'vue'

// Reactive state to track whether the mobile menu is open
const isMenuOpen = ref(false)

/**
 * toggleMenu - toggles the mobile navigation menu open/closed
 * Flips the boolean value of `isMenuOpen`.
 */
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

/**closeMenu - closes the mobile navigation menu*/
const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <!-- Navbar -->
  <nav class="navbar fixed top-0 w-full z-50 transition-colors duration-300 shadow-md">
    <!-- navbar Container -->
    <div class="nav-container max-w-[1300px] mx-auto px-6 py-3 flex justify-between items-center backdrop-blur-xl">
      <!-- Logo: brand image on the left side of the navbar -->
      <div class="nav-log">
        <img src="../../public/arro-chat-bot.png" alt="ArRo Chat Bot" class="nav-logo-img w-20 h-20"  />
      </div>

      <!-- Menu element: main navigation links-->
      <ul class="nav-menu" :class="{ active: isMenuOpen }">
        <li class="nav-item">
          <a href="#home" class="nav-link" @click="closeMenu">Home</a>
        </li>
        <li class="nav-item">
          <a href="#features" class="nav-link" @click="closeMenu">Features</a>
        </li>
        <li class="nav-item">
          <a href="#faqs" class="nav-link" @click="closeMenu">FAQs</a>
        </li>
        <li class="nav-item">
          <a href="#contact" class="nav-link" @click="closeMenu">Contact</a>
        </li>
      </ul>

      <div class="hidden md:flex gap-6">
        <button>
        Sign in
      </button>
      <button class="bg-blue-500 text-white px-5 py-3 rounded-xl font-semibold">
        Sign Up
      </button>
      </div>
      

      <!-- Navbar menu toggle: hamburger icon shown only on small screens  -->
      <div class="nav-toggle flex flex-col gap-1 cursor-pointer md:hidden" @click="toggleMenu">
        <span class="block w-6 h-[3px] bg-black rounded transition-all duration-300"></span>
        <span class="block w-6 h-[3px] bg-black rounded transition-all duration-300"></span>
        <span class="block w-6 h-[3px] bg-black rounded transition-all duration-300"></span>
      </div>
    </div>
  </nav>
  <div class="mb-30 md:mb-20 lg:mb-4"></div>
</template>

<!-- custom scoped styles for the top navigation bar. -->
<style scoped>
/* .navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: #fff;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  transition: background-color 0.3s ease;
} */

/* .nav-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
} */

/* .nav-logo a {
  font-size: 1.5rem;
  font-weight: 700;
  color: #2563eb;
  text-decoration: none;
  transition: color 0.3s ease;
} */

/* .nav-logo a:hover {
  color: #1d4ed8;
} */

.nav-menu {
  display: flex;
  list-style: none;
  gap: 2rem;
  margin: 0;
  padding: 0;
}

.nav-link {
  color: black;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
  position: relative;
  font-size: 18px;
}

.nav-link:hover{
  color: oklch(62.3% 0.214 259.815);
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: oklch(62.3% 0.214 259.815);
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

/* .nav-toggle {
  display: none;
  flex-direction: column;
  cursor: pointer;
  gap: 4px;
} */
/* 
.nav-toggle span {
  width: 25px;
  height: 3px;
  background-color: #374151;
  transition: all 0.3s ease;
  border-radius: 3px;
} */



@media (max-width: 768px) {
  .nav-toggle {
    display: flex;
  }

  .nav-menu {
    position: fixed;
    left: -100%;
    top: 100px;
    flex-direction: column;
    background-color: oklch(80.9% 0.105 251.813);
    width: 100%;
    text-align: center;
    transition: left 0.3s ease;
    padding: 2rem 0;
    gap: 0;
  }

  .nav-menu.active {
    left: 0;
  }

  .nav-item {
    padding: 1rem 0;
  }
}
</style>