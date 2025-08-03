<template>
    <section class="py-16 bg-white px-5">
        <div class="max-w-6xl mx-auto text-center">
            <h2 class="text-3xl font-bold text-orange-600 mb-4">
                Our Impact
            </h2>
            <p class="text-gray-700 mb-12">
                See how we're making a difference in the lives of many.
            </p>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-10">
                <div v-for="stat in stats" :key="stat.label"
                class="bg-gray-50 rounded-2xl shadow-md p-6">
                    <h3 class="text-4xl font-extrabold text-orange-600">
                        {{ Math.floor(stat.animatedValue) }}+
                    </h3>
                    <p class="text-gray-600 mt-2">{{ stat.label }}</p>
                </div>
            </div>
            <ImpactChart/>
        </div>
    </section>
</template>

<script setup>
import { useIntervalFn } from '@vueuse/core';
import { onMounted, ref } from 'vue';
import ImpactChart from './ImpactChart.vue';

    const stats = ref([
        {
            label:'People Helped',
            value: 12000,
            animatedValue: 0
        },
        {
            label:'Projects Completed',
            value: 240,
            animatedValue: 0
        },
        {
            label:'Years of Service',
            value:10,
            animatedValue:0
        },
        {
            label:'Communities Reached',
            value:150,
            animatedValue:0
        }
    ])

    onMounted(() => {
        stats.value.forEach((stat) => {
            const step = stat.value/60
            const {pause} = useIntervalFn(() => {
                if(stat.animatedValue < stat.value){
                    stat.animatedValue += step
                } else {
                    stat.animatedValue = stat.value
                    pause()
                }
            },16)
        })
    })
</script>