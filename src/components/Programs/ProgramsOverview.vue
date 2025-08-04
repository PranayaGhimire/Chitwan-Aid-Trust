<template>
  <section class="py-12 px-4 max-w-7xl mx-auto">
    <h2 class="text-3xl font-bold text-center mb-4">Our Programs</h2>
    <p class="text-center text-gray-600 mb-8">
      Explore our diverse programs designed to uplift communities and bring lasting impact.
    </p>

    <!-- Filter Buttons -->
    <div class="flex flex-wrap justify-center gap-4 mb-8">
      <button
        v-for="type in categories"
        :key="type"
        @click="selectedCategory = type"
        class="px-4 py-2 rounded-full border transition"
        :class="{
          'bg-orange-500 text-white': selectedCategory === type,
          'bg-white text-gray-700 hover:bg-orange-100 border-orange-500': selectedCategory !== type
        }"
      >
        {{ type }}
      </button>
    </div>

    <!-- Program Grid -->
    <div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
      <div
        v-for="program in filteredPrograms"
        :key="program.id"
        class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition"
      >
        <img :src="program.icon" alt="Program Icon" class="w-12 h-12 mb-4" />
        <h3 class="text-xl font-semibold mb-2">{{ program.name }}</h3>
        <p class="text-gray-600 text-sm mb-4">{{ program.description }}</p>
        <a href="#" class="text-orange-500 font-medium hover:underline">Learn More →</a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from 'vue'

const selectedCategory = ref('All')

const categories = [
  'All',
  'Education & Literacy',
  'Healthcare & Medical Aid',
  'Community Development',
  'Emergency Relief',
  'Women & Child Welfare',
  'Environmental Conservation'
]

const programs = ref([
  {
    id: 1,
    name: 'Health Camps',
    category: 'Healthcare & Medical Aid',
    description: 'Free medical check-ups and health awareness.',
    icon: 'https://img.icons8.com/fluency/48/stethoscope.png',
  },
  {
    id: 2,
    name: 'Scholarship Support',
    category: 'Education & Literacy',
    description: 'Helping students pursue their dreams.',
    icon: 'https://img.icons8.com/color/48/graduation-cap--v2.png',
  },
  {
    id: 3,
    name: 'Tree Plantation',
    category: 'Environmental Conservation',
    description: 'Promoting green spaces across communities.',
    icon: 'https://img.icons8.com/fluency/48/plant-under-sun.png',
  },
  {
    id: 4,
    name: 'Women Empowerment',
    category: 'Women & Child Welfare',
    description: 'Skill training and self-help groups for women.',
    icon: 'https://img.icons8.com/fluency/48/women-empowerment.png',
  },
  {
    id: 5,
    name: 'Computer Literacy',
    category: 'Education & Literacy',
    description: 'Equipping youth with digital skills.',
    icon: 'https://img.icons8.com/fluency/48/classroom.png',
  },
  {
    id: 6,
    name: 'Disaster Relief',
    category: 'Emergency Relief',
    description: 'Emergency response and aid distribution.',
    icon: 'https://img.icons8.com/fluency/48/natural-disaster.png',
  },
  {
    id: 7,
    name: 'Community Clean-Up',
    category: 'Community Development',
    description: 'Local campaigns for clean and hygienic spaces.',
    icon: 'https://img.icons8.com/fluency/48/broom.png',
  },
  {
    id: 8,
    name: 'Nutrition for Children',
    category: 'Women & Child Welfare',
    description: 'Supplemental food distribution for malnourished kids.',
    icon: 'https://img.icons8.com/fluency/48/baby-bottle.png',
  },
])

const filteredPrograms = computed(() =>
  selectedCategory.value === 'All'
    ? programs.value
    : programs.value.filter((p) => p.category === selectedCategory.value)
)
</script>
