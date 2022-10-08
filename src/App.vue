<template>

    <NavMenu></NavMenu>

    <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router';
import NavMenu from "./components/nav-menu.vue";


</script>

<style scoped>
</style>
