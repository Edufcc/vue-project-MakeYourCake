<template>
  <header>
    <Menu :logo="logo_src" :alt="app_name" />
    <router-view />
    <Footer />
  </header>
</template>

<script lang="ts">
import Vue from 'vue';
import Menu from '@/components/Menu.vue';
import Footer from '@/components/Footer.vue';

export default Vue.extend({
  components: {
    Menu,
    Footer
  },
  data() {
    return {
      logo_src: "/img/logo.png",
      app_name: "Make your cake"
    };
  }
});
</script>

<style>
  *{
    font-family: Arial, Helvetica, sans-serif;
    margin: 8px;
    padding: 0;
  }

  .main-container {
    margin: 25px;
    min-height: 300px;
  }

  h1 {
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }
</style>
