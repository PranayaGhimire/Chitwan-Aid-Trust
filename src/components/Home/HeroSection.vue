<script setup>
    import firstSlider from "../../assets/firstSlider.webp";
    import secondSlider from "../../assets/secondSlider.webp";
    import thirdSlider from "../../assets/3rdSlider.webp"; 
import { ref } from "vue";

    const currentSlide = ref(0);
</script>

<template>
    <div class="relative">
        <v-carousel  v-model ="currentSlide" cycle hide-delimiters :show-arrows="false" >
            <v-carousel-item
                :src="firstSlider"
                cover
            >
                <div 
                class=" space-y-5 absolute inset-0 flex flex-col items-center justify-center text-center text-white bg-black/50 bg-opacity-50 px-4">
                    <h1 class="text-4xl md:text-6xl font-bold drop-shadow-lg">
                         Chitwan Aid Trust
                    </h1>
                    <p class=" text-lg md:text-2xl font-medium drop-shadow-md">
                        Empowering Communities. Changing Lives.
                    </p>
                    <button class="bg-orange-600 hover:bg-orange-700 cursor-pointer p-2 rounded-lg">Donate Now</button>
                </div>
            </v-carousel-item>

            <v-carousel-item
                :src="secondSlider"
                cover
            >
                <div 
                class=" space-y-5 absolute inset-0 flex flex-col items-center justify-center text-center text-white bg-black/50 bg-opacity-50 px-4">
                    <h1 class="text-4xl md:text-6xl font-bold drop-shadow-lg">
                         Chitwan Aid Trust
                    </h1>
                    <p class=" text-lg md:text-2xl font-medium drop-shadow-md">
                        Empowering Communities. Changing Lives.
                    </p>
                    <button class="bg-orange-600 hover:bg-orange-700 cursor-pointer p-2 rounded-lg">Learn More</button>
                </div>
            </v-carousel-item>

            <v-carousel-item
                :src="thirdSlider"
                cover
            >
                <div 
                class=" space-y-5 absolute inset-0 flex flex-col items-center justify-center text-center text-white bg-black/50 bg-opacity-50 px-4">
                    <h1 class="text-4xl md:text-6xl font-bold drop-shadow-lg">
                         Chitwan Aid Trust
                    </h1>
                    <p class=" text-lg md:text-2xl font-medium drop-shadow-md">
                        Empowering Communities. Changing Lives.
                    </p>
                    <button class="bg-orange-600 hover:bg-orange-700 cursor-pointer p-2 rounded-lg">Volunteer</button>
                </div>
            </v-carousel-item>
        </v-carousel>
        <div class="flex justify-center gap-5 my-5">
            <button
            class="w-10 p-1.5 rounded-lg transition-all duration-200  hover:bg-orange-500 hover:text-white  border-2 border-orange-500 cursor-pointer"
            :class="currentSlide === index && 'bg-orange-500 text-white'" 
            v-for="(btn,index) in ['1','2','3']" :key="index" @click="currentSlide = index">
                {{ btn }}
            </button>
        </div>
    </div>
</template>