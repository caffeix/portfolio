<script setup lang="ts">
  import type { NavItem } from "@/types/nav";

  defineProps<{ items: NavItem[] }>();
</script>

<template>
  <nav>
    <ul>
      <li v-for="item in items" :key="item.href">
        <a :href="item.href">{{ item.label }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
    nav {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center
    }
    ul {
        list-style-type: none;
        display: flex;
        flex-direction: row;
        gap: 1rem;
    }
    a {
        text-decoration: none;
        text-transform: uppercase;
        color: black;
    }
</style>