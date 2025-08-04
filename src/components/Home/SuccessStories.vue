<template>
    <section class="py-16 bg-white">
        <div class="max-w-5xl mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-4">Success Stories</h2>
            <p class="text-gray-600 mb-10">Real voices from our community</p>
            
            <div class="relative">
                <!-- Slide -->
                 <div class="bg-gray-50 p-6 rounded-xl shadow-md max-w-xl mx-auto transition duration-500 "
                 
                    :key="currentTestimonial.name">
                    <div class="flex flex-col items-center">
                        <img :src="currentTestimonial.photo" :alt="currentTestimonial.name"
                        class="w-20 h-20 rounded-full mb-4 object-cover"/>
                        <h3 class="text-xl font-semibold text-gray-800">{{ currentTestimonial.name }}</h3>
                        <p class="text-gray-500 italic mt-2">{{ currentTestimonial.story }}</p>
                    </div>
                 </div>
                 <!-- Navigation -->
                 <div class="mt-6 flex justify-center gap-3">
                    <button
                    v-for="(dot,index) in testimonials" :key="index"
                    class="w-3 h-3 rounded-full"
                    :class="currentIndex === index ? 'bg-orange-600':'bg-gray-300'" 
                    @click="currentIndex = index">
                        
                    </button>
                 </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { computed, ref } from 'vue';

    const testimonials = [
        {
            name:'Aarati Thapa',
            story: 'Because of Chitwan Aid Trust, I now have a small business and can support my children’s education.',
            photo: 'https://randomuser.me/api/portraits/women/44.jpg',
        },
        {
            name: 'Ramesh Gurung',
            story: 'They helped rebuild our home after the flood. I’m forever grateful.',
            photo: 'https://randomuser.me/api/portraits/men/32.jpg',
        },
        {
            name: 'Maya Lama',
            story: 'I learned tailoring through their training and now earn a steady income.',
            photo: 'https://randomuser.me/api/portraits/women/68.jpg',
        },
    ] 

    const currentIndex = ref(0);
    const currentTestimonial = computed(() => testimonials[currentIndex.value])
</script>