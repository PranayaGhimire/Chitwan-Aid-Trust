<template>
    <nav class="bg-white p-5 space-y-5">
        <div class="flex justify-between md:justify-around items-center h-20 ">
            <div class="overflow-hidden">
              <img :src="chitwanLogo" alt="" class="object-cover">
            </div>
            <ul class="hidden md:flex gap-10 ">
                <li v-for="(link,index) in links" :key="index">
                    <RouterLink :to= "link.route" class="hover:text-orange-600" active-class="text-orange-600">
                        {{ link.name }}
                    </RouterLink> 
                </li>
            </ul>
            <Bars3Icon class="md:hidden w-10 h-10" @click="toggleMenu"/>
        </div>
        <!-- Mobile Menu -->
        <transition
            name="slide"
            enter-active-class="transition duration-200 ease-out"
            leave-active-class="transition duration-300 ease-in"
            enter-from-class="opacity-0 -translate-y-5"
            enter-to-class="opacity-100 translate-y-0"
            leave-to-class="opacity-0 -translate-y-5"
        >
            <ul v-if="isOpen" class="ml-3 space-y-2">
                <li v-for="(link,index) in links" :key="index">
                    <RouterLink :to="link.route" active-class="text-orange-600" @click="closeMenu">
                        {{ link.name }}
                    </RouterLink>
                </li>
            </ul>
        </transition>
      
    </nav>
</template>

<script setup>
    import { ref } from "vue";
import chitwanLogo from "../assets/chitwanlogo.png";
    import {Bars3Icon} from "@heroicons/vue/24/solid"

    const isOpen = ref(false);

    const toggleMenu = () => {
        isOpen.value = !isOpen.value;
    }

    const closeMenu = () => {
        isOpen.value = false;
    }

    const links = [
        {
            name:'Home',
            route:'/'
        },
        {
            name:'About',
            route:'/about'
        },
        {
            name:'Programs',
            route:'/programs'
        },
        {
            name:'Get Involved',
            route:'/getInvolved'
        },
        {
            name:'Donate',
            route:'/donate'
        },
        {
            name:'Contact',
            route:'/contact'
        }
    ]
</script>

<style>

</style>