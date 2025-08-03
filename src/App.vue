<script setup>
import {  RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <Header/>
  <Navbar/>
  <RouterView />
  <Footer/>
</template>

<style scoped>

</style>
