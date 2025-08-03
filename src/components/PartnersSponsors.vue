<template>
  <section class="py-16 bg-gray-50">
    <div class="max-w-6xl mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold mb-6 text-gray-800">Our Partners & Sponsors</h2>
      <p class="text-gray-600 mb-10">We’re proud to be supported by these incredible organizations.</p>

      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-6 items-center">
        <img v-for="(logo, index) in logos" :key="index" :src="logo" class="h-16 object-contain grayscale hover:grayscale-0 transition" />
      </div>

      <div class="mt-12">
        <button class="bg-orange-600 hover:bg-orange-700 text-white px-6 py-3 rounded-xl shadow font-semibold">
          Become a Partner
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const logos = [
  "https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/Unicef_Logo.svg/2560px-Unicef_Logo.svg.png",
  "https://upload.wikimedia.org/wikipedia/commons/5/5d/USAID-Logo.svg",
  "https://upload.wikimedia.org/wikipedia/commons/9/98/Red_Cross_Logo.svg",
  "https://upload.wikimedia.org/wikipedia/commons/1/12/World_Health_Organization_Logo.svg",
  "https://upload.wikimedia.org/wikipedia/commons/5/5a/WWF_logo.svg",
  "https://upload.wikimedia.org/wikipedia/commons/3/3f/Nepal_Government_Logo.svg",
  "https://upload.wikimedia.org/wikipedia/commons/5/55/Oxfam_logo.svg",
  "https://upload.wikimedia.org/wikipedia/commons/b/b4/Rotary_International_logo.svg"
];
</script>
