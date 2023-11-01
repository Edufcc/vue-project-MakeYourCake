
<template>
  <header>
    <Menu/>
    <router-view/>
    <Footer/>
  </header>
</template>


<script setup lang="ts">
import { RouterView } from 'vue-router';
import Menu from '@/components/Menu.vue';
import Footer from '@/components/Footer.vue';
import HomeView from './views/HomeView.vue';
</script>

<style scoped></style>
