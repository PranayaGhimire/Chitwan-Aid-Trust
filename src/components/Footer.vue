<template>
  <footer class="bg-gray-900 text-white py-10 px-5">
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-8">

      <!-- Quick Links -->
      <div>
        <h3 class="text-lg font-semibold mb-3">Quick Links</h3>
        <ul class="space-y-2 text-sm text-gray-300">
          <li><RouterLink to="/">Home</RouterLink></li>
          <li><RouterLink to="/programs">Programs</RouterLink></li>
          <li><RouterLink to="/about">About Us</RouterLink></li>
          <li><RouterLink to="/contact">Contact</RouterLink></li>
        </ul>
      </div>

      <!-- Newsletter -->
      <div>
        <h3 class="text-lg font-semibold mb-3">Newsletter</h3>
        <p class="text-sm text-gray-400 mb-3">Subscribe to get our latest updates.</p>
        <div class="flex flex-col sm:flex-row items-center gap-2">
          <input
            type="email"
            placeholder="Your email"
            class="px-3 py-2 rounded bg-gray-800 text-white w-full"
          />
          <button class="bg-orange-500 text-white px-4 py-2 rounded hover:bg-orange-600">
            Subscribe
          </button>
        </div>
      </div>

      <!-- Contact Info -->
      <div>
        <h3 class="text-lg font-semibold mb-3">Contact Info</h3>
        <div class="flex items-start gap-2 text-sm text-gray-300">
          <MapPinIcon class="w-5 h-5 text-orange-400 mt-1" />
          <span> Bharatpur, Chitwan, Nepal</span>
        </div>
        <div class="flex items-center gap-2 mt-2 text-sm text-gray-300">
          <EnvelopeIcon class="w-5 h-5 text-orange-400" />
          <span>info@chitwanaidtrust.org</span>
        </div>
        <div class="flex items-center gap-2 mt-2 text-sm text-gray-300">
          <PhoneIcon class="w-5 h-5 text-orange-400" />
          <span>+977-9800000000</span>
        </div>
      </div>

      <!-- Social Media -->
      <div>
        <h3 class="text-lg font-semibold mb-3">Follow Us</h3>
        <div class="flex space-x-4">
          <a href="#" class="text-gray-300 hover:text-white">
            <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-5 h-5" viewBox="0 0 24 24"><path d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.877v-6.99h-2.54v-2.887h2.54V9.797c0-2.506 1.493-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.465h-1.26c-1.243 0-1.63.772-1.63 1.562v1.875h2.773l-.443 2.887h-2.33v6.99C18.343 21.128 22 16.991 22 12z"/></svg>
          </a>
          <a href="#" class="text-gray-300 hover:text-white">
            <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-5 h-5" viewBox="0 0 24 24"><path d="M21.35 6.07a8.38 8.38 0 0 1-2.357.646 4.118 4.118 0 0 0 1.804-2.27 8.224 8.224 0 0 1-2.605.977 4.107 4.107 0 0 0-6.993 3.743A11.65 11.65 0 0 1 3.1 4.9a4.106 4.106 0 0 0 1.27 5.482 4.073 4.073 0 0 1-1.86-.514v.052a4.107 4.107 0 0 0 3.292 4.024 4.095 4.095 0 0 1-1.852.07 4.108 4.108 0 0 0 3.834 2.85A8.233 8.233 0 0 1 2 19.54a11.616 11.616 0 0 0 6.29 1.84c7.547 0 11.675-6.253 11.675-11.675 0-.178-.004-.355-.012-.53A8.345 8.345 0 0 0 22 6.545a8.216 8.216 0 0 1-2.357.646z"/></svg>
          </a>
          <a href="#" class="text-gray-300 hover:text-white">
            <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="w-5 h-5" viewBox="0 0 24 24"><path d="M19.615 3H4.385A1.385 1.385 0 0 0 3 4.385v15.23A1.385 1.385 0 0 0 4.385 21h15.23A1.385 1.385 0 0 0 21 19.615V4.385A1.385 1.385 0 0 0 19.615 3zm-8.23 14.385H8.615v-6.23h2.77v6.23zm-1.385-7.615a1.615 1.615 0 1 1 0-3.23 1.615 1.615 0 0 1 0 3.23zm9.615 7.615h-2.77v-3.23c0-.77-.77-1.385-1.615-1.385s-1.615.615-1.615 1.385v3.23h-2.77v-6.23h2.77v.77c.615-.385 1.615-.77 2.77-.77 1.54 0 2.77 1.23 2.77 2.77v3.46z"/></svg>
          </a>
        </div>
      </div>
    </div>

    <!-- Bottom Footer -->
    <div class="border-t border-gray-700 mt-10 pt-4 text-center text-sm text-gray-400">
      © 2025 Chitwan Aid Trust. All rights reserved.
    </div>
  </footer>
</template>

<script setup>
import { MapPinIcon, EnvelopeIcon, PhoneIcon } from "@heroicons/vue/24/outline";
</script>
