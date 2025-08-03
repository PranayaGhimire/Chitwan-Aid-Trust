<script setup>
    import {Chart as ChartJS, ArcElement, Legend, Title, Tooltip } from "chart.js";
    import {Pie} from "vue-chartjs"

     ChartJS.register(Title, Tooltip, Legend, ArcElement)
     
     const chartData = {
        labels: ['Health','Education','Food Distribution','Shelter'],
        datasets:[
            {
                label: 'Support Distribution',
                backgroundColor: ['#14b8a6', '#f59e0b', '#6366f1', '#ef4444'],
                data: [40, 30, 20, 10],
            },
        ],
     }

     const chartOptions = {
        responsive:true,
        plugins:{
            legend:{
                position:'bottom'
            },
        },
     }
</script>

<template>
    <div class="mt-10 max-w-md mx-auto">
        <Pie :data="chartData" :options="chartOptions"/>
    </div>
</template>