<script setup>
    import ProgramsOverview from "@/components/ProgramsOverview.vue";
import bgImage from "../assets/sunrise-in-chitwan.webp"
import ProgramCategories from "@/components/ProgramCategories.vue";
import ProgramCards from "@/components/ProgramCards.vue";
import HowToHelp from "@/components/HowToHelp.vue";
</script>

<template>
    <main>
        <div class="px-5 md:px-12 lg:px-26 xl:px-44 2xl:px-54 py-26 space-y-5 bg-cover bg-center bg-no-repeat opacity-100"
            :style="{ backgroundImage: `url(${bgImage})`}">
                <h1 class="text-4xl font-bold text-white">Programs</h1>
                <hr class="w-14 border-2 border-orange-600"/>
        </div>
        <ProgramsOverview/>
        <ProgramCategories/>
        <ProgramCards/>
        <HowToHelp/>
    </main>

</template>


