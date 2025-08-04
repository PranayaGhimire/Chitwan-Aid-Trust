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
          class="h-48 w-full object-cover rounded-md mb-4"
        />
        <h3 class="text-xl font-semibold mb-2">{{ program.title }}</h3>
        <p class="text-gray-600 mb-3" v-if="program.description">{{ program.description }}</p>
        <p class="text-sm text-gray-500 mb-4" v-if="program.target">
          🎯 Target: {{ program.target }}
        </p>
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
    title: 'Quality Education for All',
    description: 'Providing access to learning materials and teacher training in rural schools.',
    target: 'Children aged 6–14 in remote villages',
    image: 'https://source.unsplash.com/400x300/?education,school'
  },
  {
    title: 'Mobile Health Clinics',
    description: 'Bringing healthcare to underserved communities through mobile units.',
    target: 'Rural families without access to hospitals',
    image: 'https://source.unsplash.com/400x300/?healthcare,clinic'
  },
  {
    title: 'Women Empowerment Workshops',
    description: 'Skills training and literacy classes to support self-reliance.',
    target: 'Women and girls in low-income areas',
    image: 'https://source.unsplash.com/400x300/?women,training'
  },
  {
    title: 'Clean Water Access',
    description: 'Installing water filters and wells in water-scarce areas.',
    target: 'Villages in drought-prone regions',
    image: 'https://source.unsplash.com/400x300/?water,clean'
  },
  {
    title: 'Emergency Disaster Relief',
    description: 'Immediate aid and recovery support during natural disasters.',
    target: 'Flood and landslide victims',
    image: 'https://source.unsplash.com/400x300/?disaster,relief'
  },
  {
    title: 'Tree Plantation Drives',
    description: 'Engaging communities in reforestation and awareness programs.',
    target: 'Schoolchildren and local farmers',
    image: 'https://source.unsplash.com/400x300/?tree,plantation'
  }
]
</script>
