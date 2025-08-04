<template>
    <section class="py-12 px-5 bg-white">
        <div class="max-w-6xl mx-auto text-center space-y-5">
            <!-- Mission -->
             <div class="space-y-2">
                <h2 class="text-3xl font-bold text-orange-600">Our Mission</h2>
                <p class="text-lg text-gray-700">
                   The charitable objectives of the Company would be for the public benefit in any part of the world but primarily in support of people in the remote areas of Chitwan district of Nepal. The activities include providing relief and assistance of people who are the victims of natural disaster, trouble, or catastrophe and to advance education for the benefit of the public in particular but not exclusively by building schools and providing access to educational facilities such as libraries as well as providing relief of sickness and the preservation of health by providing or assisting in the provision of healthcare projects. 
                </p>
             </div>
            <!-- Vision -->
            <div>
                 <h2 class="text-3xl font-bold text-orange-600 ">Our Vision</h2>
                 <p class="text-lg text-gray-700">
                    A world where every community thrives through unity, empowerment, and access to basic human needs.
                 </p>
            </div> 
            <!-- Core Values -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <div
                v-for="(value,index) in values"
                :key="index"
                class="p-6 bg-white rounded-2xl shadow-md transition-transform hover:scale-105 cursor-pointer space-y-1">
                    <component
                    :is="value.icon"
                    class="h-10 w-10 text-orange-600 mx-auto"/>
                    <h3 class="font-semibold text-xl text-gray-800">{{ value.title }}</h3>
                    <p class="text-sm text-gray-600">{{ value.description }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { AcademicCapIcon, EyeIcon, HeartIcon, ShieldCheckIcon } from '@heroicons/vue/24/solid';

    const values = [
        {
            title:'Integrity',
            description: 'We act with honesty and uphold strong moral principles in every effort.',
            icon:ShieldCheckIcon
        },
        {
            title:'Compassion',
            description:'We care deeply for the communities we serve and act with empathy.',
            icon: HeartIcon
        },
        {
            title:'Transparency',
            description:'We ensure openness in our operations and communication.',
            icon:EyeIcon
        },
        {
            title:'Empowerment',
            description:'We equip individuals with tools and opportunities for self-growth.',
            icon: AcademicCapIcon
        }
    ]
</script>