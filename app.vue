<template>
  <div class="min-h-screen w-full">
    <!-- Navigation Bar -->
    <nav 
      class="fixed top-0 w-full py-4 px-6 flex items-center justify-between transition-all duration-300 z-50"
      :class="[
        scrollY > 0 ? 'bg-white dark:bg-gray-900 shadow-sm' : 'bg-transparent text-gray-400', 
        isNavVisible ? 'translate-y-0' : '-translate-y-full'
      ]"
    >
      <!-- Logo/Brand -->
      <div class="font-text text-size-5 font-800 uppercase">
        <NuxtLink to="/" class="hover:opacity-80 transition-opacity">
          Naggib
        </NuxtLink>
      </div>
      
      <!-- Navigation Items -->
      <div class="hidden md:flex items-center space-x-12 uppercase font-title text-size-4 font-700">
        <NuxtLink to="/services" class="hover:text-primary-500 transition-colors">Services</NuxtLink>
        <NuxtLink to="/clients" class="hover:text-primary-500 transition-colors">Clients</NuxtLink>
        <NuxtLink to="/who-i-help" class="hover:text-primary-500 transition-colors">Who I Help</NuxtLink>
        <NuxtLink to="/blog" class="hover:text-primary-500 transition-colors">Blog</NuxtLink>
        <NuxtLink to="/about" class="hover:text-primary-500 transition-colors">About</NuxtLink>
      </div>
      
      <!-- CTA Button -->
       <UButton
       label="Let's talk"
       btn="solid-black"
       rounded="full"
       class="hidden md:block hover:text-white font-600 hover:bg-primary hover:scale-102 active:scale-99 transition-all duration-300"
       link
       to="/contact"
       />
      
      <!-- Mobile Menu Button (only visible on small screens) -->
      <button class="md:hidden" @click="mobileMenuOpen = !mobileMenuOpen">
        <span class="i-heroicons-bars-3 text-2xl"></span>
      </button>
    </nav>
    
    <!-- Mobile Menu (only visible when toggled) -->
    <div 
      v-if="mobileMenuOpen" 
      class="fixed top-[72px] left-0 right-0 md:hidden bg-white dark:bg-gray-900 shadow-md py-4 px-6 z-40"
    >
      <div class="flex flex-col space-y-4">
        <NuxtLink to="/services" class="hover:text-primary-500 transition-colors">SERVICES</NuxtLink>
        <NuxtLink to="/clients" class="hover:text-primary-500 transition-colors">CLIENTS</NuxtLink>
        <NuxtLink to="/who-i-help" class="hover:text-primary-500 transition-colors">WHO I HELP</NuxtLink>
        <NuxtLink to="/resources" class="hover:text-primary-500 transition-colors">RESOURCES</NuxtLink>
        <NuxtLink to="/about" class="hover:text-primary-500 transition-colors">ABOUT</NuxtLink>
        <NuxtLink to="/contact" class="bg-primary-500 hover:bg-primary-600 text-white px-6 py-2 rounded-md transition-colors text-center">
          Let's talk
        </NuxtLink>
      </div>
    </div>
    
    <!-- Page Content -->
    <div class="pt-16"> <!-- Add padding to account for fixed navbar -->
      <NuxtPage />
    </div>

    <!-- Footer -->
     <Footer />
  </div>
</template>

<script lang="ts" setup>
import '@una-ui/preset/una.css'

// State for mobile menu
const mobileMenuOpen = ref(false)

// Scroll position tracking
const scrollY = ref(0)
const lastScrollY = ref(0)
const isNavVisible = ref(true)

// Update scroll position and control navbar visibility
const handleScroll = () => {
  scrollY.value = window.scrollY
  
  // Show/hide navbar based on scroll direction
  if (scrollY.value < lastScrollY.value || scrollY.value < 50) {
    // Scrolling up or near the top - show navbar
    isNavVisible.value = true
  } else if (scrollY.value > lastScrollY.value && scrollY.value > 50) {
    // Scrolling down and not at the top - hide navbar
    isNavVisible.value = false
  }
  
  lastScrollY.value = scrollY.value
}

// Add scroll event listener when component is mounted
onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
})

// Remove event listener when component is unmounted
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

useHead({
  meta: [
    { name: 'view-transition', content: 'same-origin' }
  ]
})
</script>

<style>
html {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

body {
  margin: 0;
  padding: 0;
}

[tooltip~="black"] {
  border: none;
}

.tooltip-content {
  padding: 0px;
}


div[data-radix-menu-content] {
  backdrop-filter: blur(5px);
  background-color: rgb(255 255 255 / 0.6) /* #fff */;
}

.dark div[data-radix-menu-content] {
  backdrop-filter: blur(5px);
  background-color: rgb(0 0 0 / 0.6) /* #000 */;
}
</style>
