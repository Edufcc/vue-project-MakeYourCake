<template>
    <nav id="menu">
        
            <router-link to="/" id="logo-url">
                <img :src="logo" :alt="alt" id="logo">
            </router-link>
            <router-link to="/">Home</router-link>
            <router-link to="/orders">Pedidos</router-link>
       
    </nav>
</template>

<script setup lang="ts">
    import { defineProps } from 'vue';

    const props = defineProps({
        logo: String,
        alt: String
    });

</script>

<style scoped>
    #menu {
        background-color: var(--gray-color);
        border-radius: 25px;
        padding: 15px 50px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }

    #logo-url {
        margin: auto;
        margin-left: 0;
    }

    #logo {
        width: 50px;
    }

    a {
        color: var(--bg-color);
        text-decoration: none;
        margin: 12px;
        transition: .5s;
    }

    a:hover {
        color: #111;
    }

</style>