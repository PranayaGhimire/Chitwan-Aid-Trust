<template>
  <section class="py-16 px-4 bg-gray-50">
    <div class="max-w-7xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-4">How You Can Help</h2>
      <p class="text-gray-600 mb-10 max-w-2xl mx-auto">
        Your support empowers us to make lasting changes in the lives of people across Nepal.
        Choose how you'd like to contribute.
      </p>

      <div class="grid gap-8 md:grid-cols-3">
        <div
          v-for="option in helpOptions"
          :key="option.title"
          class="bg-white rounded-xl shadow p-6 hover:shadow-lg transition"
        >
          <component :is="option.icon" class="h-12 w-12 text-orange-600 mb-4 mx-auto" />
          <h3 class="text-xl font-semibold mb-2">{{ option.title }}</h3>
          <p class="text-gray-600 mb-4">{{ option.description }}</p>
          <button
            class="inline-block px-4 py-2 bg-orange-600 hover:bg-orange-700 text-white rounded-md font-medium"
          >
            {{ option.button }}
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { HeartIcon, UserGroupIcon, HandRaisedIcon } from '@heroicons/vue/24/outline'

const helpOptions = [
  {
    title: 'Donate to a Cause',
    description:
      'Support our initiatives by making a one-time or recurring donation to your chosen program.',
    icon: HeartIcon,
    button: 'Donate Now'
  },
  {
    title: 'Volunteer with Us',
    description:
      'Join hands with our teams on the ground and be part of meaningful change in communities.',
    icon: UserGroupIcon,
    button: 'Become a Volunteer'
  },
  {
    title: 'Partner with Us',
    description:
      'Collaborate as a government body, NGO, or corporate sponsor to expand our reach and impact.',
    icon: HandRaisedIcon,
    button: 'Start a Partnership'
  }
]
</script>
