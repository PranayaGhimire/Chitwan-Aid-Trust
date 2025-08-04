<template>
  <section class="py-12 px-4 max-w-7xl mx-auto">
    <h2 class="text-3xl font-bold text-center mb-8">Our Key Programs</h2>

    <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
      <div
        v-for="program in programs"
        :key="program.title"
        class="bg-white rounded-xl shadow hover:shadow-lg transition p-6 flex flex-col"
      >
        <img
          :src="program.image"
          :alt="program.title"
          class="h-48 w-full  rounded-md mb-4"
        />
        <h3 class="text-xl font-semibold mb-2">{{ program.title }}</h3>
        <button
          class="mt-auto inline-block px-4 py-2 bg-orange-600 hover:bg-orange-700 text-white rounded-md font-semibold"
        >
          Support This Program
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
const programs = [
  {
    title: 'Blood Donation Program',
    image: 'https://chitwanaidtrust.org/uploads/photo/51.jpeg'
  },
  {
    title: 'School Donation Program',
    image: 'https://chitwanaidtrust.org/uploads/photo/25.jpeg'
  },
  {
    title: 'Parbatipur High School Donation',
    image: 'https://chitwanaidtrust.org/uploads/photo/333.jpeg'
  },
  {
    title: '100 Student Sponsorship Program',
    image: 'https://chitwanaidtrust.org/uploads/photo/336.jpeg'
  },
  {
    title: 'Nepali Mela',
    image: 'https://chitwanaidtrust.org/uploads/photo/209.jpeg'
  },
  {
    title: 'Charity Event',
    image: 'https://chitwanaidtrust.org/uploads/photo/217.jpeg'
  }
]
</script>
