<template>
  <footer class="py-24 bg-gray-50 dark:bg-[#11111B]">
    <div class="container mx-auto px-8">
      <div class="max-w-6xl mb-12 mx-auto flex flex-col items-center">
        <h1 class="font-text font-600 text-size-6">Naggib</h1>
        <p class="text-gray-400">© {{ new Date().getFullYear() }} Naggib. All rights reserved.</p>
        <p class="text-gray-600 text-size-4">
          •
        </p>
      </div>

      <div class="max-w-6xl mx-auto grid px-4 grid-cols-1 md:grid-cols-3 md:px-0 gap-8">
        <!-- Contact Information -->
        <div class="col-span-1">
          <h3 class="text-xl text-size-4 font-title font-600 uppercase mb-4">
            Contact
          </h3>

          <ul class="space-y-2 text-gray-600">
            <li class="flex items-center">
              <span class="i-ph-phone-call mr-2"></span>
              <a href="tel:07595377254" class="hover:text-primary-500 transition-colors">07595 377254 (London)</a>
            </li>
            <li class="flex items-center">
              <span class="i-ph-phone-call mr-2"></span>
              <a href="tel:+41792919650" class="hover:text-primary-500 transition-colors">tel:+41792919650 (Geneva)</a>
            </li>
          </ul>

          <div class="mt-6 flex space-x-4 text-gray-600">
            <a href="http://linkedin.com/in/naggibc" target="_blank" class="hover:text-primary-500 transition-colors">
              <span class="i-ph-linkedin-logo text-2xl"></span>
            </a>
            <a href="https://twitter.com/naggibc" target="_blank" class="hover:text-primary-500 transition-colors">
              <span class="i-ph-x-logo text-2xl"></span>
            </a>
            <a href="https://www.instagram.com/naggibc/" target="_blank" class="hover:text-primary-500 transition-colors">
              <span class="i-ph-instagram-logo text-2xl"></span>
            </a>
          </div>
        </div>

        <!-- Navigation Links -->
        <div class="col-span-1">
          <h3 class="text-size-4 font-title font-600 uppercase mb-4">Quick Links</h3>
          <ul class="space-y-2 text-gray-600">
            <li><NuxtLink to="/" class="hover:text-primary-500 transition-colors">Home</NuxtLink></li>
            <li><NuxtLink to="/about" class="hover:text-primary-500 transition-colors">About</NuxtLink></li>
            <li><NuxtLink to="/services" class="hover:text-primary-500 transition-colors">Services</NuxtLink></li>
            <li><NuxtLink to="/testimonials" class="hover:text-primary-500 transition-colors">Testimonials</NuxtLink></li>
            <li><NuxtLink to="/contact" class="hover:text-primary-500 transition-colors">Contact</NuxtLink></li>
          </ul>
        </div>

        <!-- About Section -->
        <div class="col-span-1 md:col-span-1">
          <h3 class="text-size-4 font-title font-600 uppercase mb-4">About</h3>
          <p class="font-400 text-gray-600 mb-4">
            I am an experienced executive coach, leadership development consultant 
            and corporate trainer with over 20 years international experience of leading 
            and building highly effective teams.
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>
