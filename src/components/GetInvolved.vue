<template>
  <section class="bg-orange-50 py-16">
    <div class="max-w-6xl mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold text-gray-800 mb-4">Get Involved</h2>
      <p class="text-gray-600 mb-10">Join hands with Chitwan Aid Trust and help make a difference in our communities.</p>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Volunteer -->
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition duration-300">
          <div class="text-orange-600 mb-4 flex justify-center">
            <HandRaisedIcon class="h-12 w-12" />
          </div>
          <h3 class="text-xl font-semibold mb-2">Volunteer</h3>
          <p class="text-gray-600 mb-4">Lend your time and skills to support our mission on the ground.</p>
          <button class="bg-orange-600 text-white px-4 py-2 rounded-full hover:bg-orange-700 transition">
            Join as Volunteer
          </button>
        </div>

        <!-- Partnership -->
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition duration-300">
          <div class="text-orange-600 mb-4 flex justify-center">
            <UserGroupIcon class="h-12 w-12" />
          </div>
          <h3 class="text-xl font-semibold mb-2">Partnership</h3>
          <p class="text-gray-600 mb-4">Partner with us to create long-lasting social impact in Chitwan and beyond.</p>
          <button class="bg-orange-600 text-white px-4 py-2 rounded-full hover:bg-orange-700 transition">
            Partner With Us
          </button>
        </div>

        <!-- Fundraising -->
        <div class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition duration-300">
          <div class="text-orange-600 mb-4 flex justify-center">
            <CurrencyDollarIcon class="h-12 w-12" />
          </div>
          <h3 class="text-xl font-semibold mb-2">Fundraising</h3>
          <p class="text-gray-600 mb-4">Contribute to or organize fundraising events that support our causes.</p>
          <button class="bg-orange-600 text-white px-4 py-2 rounded-full hover:bg-orange-700 transition">
            Support Fundraising
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { HandRaisedIcon, UserGroupIcon, CurrencyDollarIcon } from '@heroicons/vue/24/solid'
</script>
