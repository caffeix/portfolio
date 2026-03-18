<script setup lang="ts">
  import type { NavItem } from "@/types/nav";
  import Navbar from "./Navbar.vue";

  defineProps<{ navItems: NavItem[] }>();
</script>

<template>
  <header>
    <h1>Digital portfolio</h1>
    <Navbar :items="navItems" />
  </header>
</template>

<style scoped>
    header {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center
    }
</style>