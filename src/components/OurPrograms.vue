<template>
    <section class="py-16 bg-gray-50">
        <div class="max-w-6xl mx-auto px-4 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-4">Our Programs</h2>
            <p class="text-gray-600 mb-10">
                Empowering communities through impactful programs and initiatives.
            </p>

            <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
                <div v-for="(program,index) in programs" :key="index"
                class="bg-white p-6 rounded-xl shadow-md hover:shadow-lg transition-all">
                    <div class="flex justify-center mb-4 text-orange-600">
                        <component :is="program.icon" class="h-12 w-12"/>
                    </div>
                    <h3 class="text-xl font-semibold mb-2 text-gray-800">
                        {{ program.name }}
                    </h3>
                    <p class="text-gray-600 mb-4">
                        {{ program.description }}
                    </p>
                    <a href="" class="text-orange-600 font-semibold hover:underline inline-block">
                        Learn More
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { AcademicCapIcon, BriefcaseIcon, GlobeAltIcon, HeartIcon, HomeIcon } from '@heroicons/vue/24/solid';

    const programs = [
        {
            name:'Education Support',
            description:'Providing resources and scholarships to underprivileged students.',
            icon: AcademicCapIcon,
        },
        {
            name:'Healthcare Access',
            description:'Free medical camps and health awareness campaigns.',
            icon: HeartIcon
        },
        {
            name:"Housing for All",
            description: 'Building safe shelters for homeless families.',
            icon: HomeIcon
        },
        {
            name:'Women Empowerment',
            description:'Training and support programs for women and girls.',
            icon: BriefcaseIcon
        },
        {
            name:'Global Outreach',
            description:'Connecting with international partners to expand impact.',
            icon:GlobeAltIcon
        }
    ]
</script>