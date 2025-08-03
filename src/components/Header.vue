<template>
    <header class="lg:pl-24 flex justify-around items-center bg-orange-600 h-14 text-white">
        <div class="hidden lg:flex space-x-10">
            <p>EMAIL: info@chitwanaidtrust.org</p>
            <p>PHONE: 07735567548; Surya Bahadur Tamang, General Secretary</p>
        </div>
        <button @click="router.push('/donate')" class="w-42 h-full bg-zinc-800 cursor-pointer">
            Donate Now
        </button>
    </header>
</template>

<script setup>
import { useRouter } from 'vue-router';

    const router = useRouter();
</script>