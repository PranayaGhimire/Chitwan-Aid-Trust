<template>
  <section class="py-12 bg-gray-50 px-4 max-w-7xl mx-auto">
    <h2 class="text-3xl font-bold text-center mb-4">Program Categories</h2>
    <p class="text-center text-gray-600 mb-8">
      We focus on a wide range of categories to serve the community better.
    </p>

    <div class="grid gap-6 sm:grid-cols-2 md:grid-cols-3">
      <div
        v-for="category in categories"
        :key="category.name"
        class="bg-white p-6 rounded-xl shadow hover:shadow-lg transition text-center"
      >
        <component :is="category.icon" class="w-10 h-10 text-orange-500 mx-auto mb-4" />
        <h3 class="text-xl font-semibold">{{ category.name }}</h3>
      </div>
    </div>
  </section>
</template>

<script setup>
import {
  BookOpenIcon,
  HeartIcon,
  UsersIcon,
  ExclamationTriangleIcon,
  UserGroupIcon,
  GlobeAltIcon
} from '@heroicons/vue/24/outline'

const categories = [
  { name: 'Education & Literacy', icon: BookOpenIcon },
  { name: 'Healthcare & Medical Aid', icon: HeartIcon },
  { name: 'Community Development', icon: UsersIcon },
  { name: 'Emergency Relief', icon: ExclamationTriangleIcon },
  { name: 'Women & Child Welfare', icon: UserGroupIcon },
  { name: 'Environmental Conservation', icon: GlobeAltIcon }
]
</script>
