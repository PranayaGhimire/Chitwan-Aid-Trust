<template>
  <section class="py-16 bg-gray-50">
    <div class="max-w-6xl mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold mb-6 text-gray-800">Our Partners & Sponsors</h2>
      <p class="text-gray-600 mb-10">We’re proud to be supported by these incredible organizations.</p>

      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-6 items-center">
          <a
            v-for="partner in partners"
            :key="partner.name"
            :href="partner.link"
            target="_blank"
            rel="noopener"
            class="rounded-xl bg-white p-4 shadow hover:shadow-lg transition"
          >
            <img
              :src="partner.src"
              :alt="partner.name"
              class="h-16 mx-auto object-contain"
            />
            <span class="block mt-2 text-gray-700 text-sm">{{ partner.name }}</span>
          </a>
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
const partners = [
  {
    name: 'National Trust for Nature Conservation',
    src: 'https://upload.wikimedia.org/wikipedia/en/thumb/c/c9/National_Trust_for_Nature_Conservation_logo.svg/512px-National_Trust_for_Nature_Conservation_logo.svg.png',
    link: 'https://www.ntnc.org.np/'
  },
  {
    name: 'BCC – NTNC Biodiversity Conservation Center',
    src: 'https://upload.wikimedia.org/wikipedia/en/thumb/c/c9/National_Trust_for_Nature_Conservation_logo.svg/512px-National_Trust_for_Nature_Conservation_logo.svg.png',
    link: 'https://www.ntnc.org.np/project/biodiversity-conservation-center-bcc'
  }
];
</script>
