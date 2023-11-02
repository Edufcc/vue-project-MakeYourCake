<template>
    <div id="main-banner">
      <h1>Make your Cake</h1>
    </div>
</template>

<script setup lang="ts">

    
</script>

<style scoped>
    #main-banner {
        background-image: url("/img/cake.jpg");
        background-position: 0 -375px;
        background-size: cover;
        border-radius: 25px;
        height: 500px;
        display: flex;
        align-items: center;
        justify-content: flex-start;
    }

    #main-banner h1 {
        color: var(--bg-color);
        text-align: center;
        font-size: 60px;
    }
</style>